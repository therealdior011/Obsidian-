---
type: error
title: bash-heredoc-backslashni-yeydi
date: 2026-08-30
status: confirmed
verified: false
---

2026-08-30 MUHIT TUZOG'I: Bash tool orqali heredoc (<<'PY') ichida yozilgan matnda BIR DARAJA backslash yo'qoladi. Ya'ni Python manbasidagi '\n' faylga HAQIQIY QATOR TASHLASH bo'lib tushadi va JS satri yopilmay qoladi (SyntaxError: Invalid or unexpected token). Xuddi shu sabab \' ham ' bo'lib qoladi. IKKI MARTA yiqildim. YECHIM: (1) backslashli kodni Write tool bilan alohida faylga yozib, keyin Python bilan ulash, yoki (2) String.fromCharCode(10) ishlatish. Heredoc orqali backslash o'tkazmaslik kerak.

*<- [[hub|Xarita]]*
