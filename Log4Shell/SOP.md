
---

### 📁 Path: `Log4Shell/SOP.md`
```markdown
# 📜 SOP: Log4Shell Remediation Workflow

## 🧭 Goal
Remediate unsafe logging patterns that enable JNDI-based remote code execution.

## 🪜 Steps
1. Identify logging sinks using CodeQL
2. Trace input sources for user-controlled data
3. Sanitize input or remove logging
4. Disable JNDI in Log4j config
5. Submit PR with annotated fix and teachback.md

## ✅ Success Criteria
- No unsafe logging of user input
- Fix includes annotated logic and legacy artifact
