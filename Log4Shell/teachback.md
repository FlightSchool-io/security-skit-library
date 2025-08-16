# 🧠 Teachback: Log4Shell Remediation

## 🔍 Vulnerability
Unsafe logging of user input triggers JNDI lookup via Log4j.

## 🛠️ Fix Strategy
- Sanitize input before logging
- Disable JNDI lookups in Log4j config
- Use CodeQL to trace untrusted input to logging sinks

## 📚 CodeQL Query
```ql
import java
from LoggingSink sink, DataFlow::PathNode source
where source.asExpr() = sink.getLoggedExpr()
and source.isUserInput()
select sink, source, "Unsafe logging of user input"
