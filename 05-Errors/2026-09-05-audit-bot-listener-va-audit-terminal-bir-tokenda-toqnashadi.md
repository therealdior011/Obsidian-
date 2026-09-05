---
type: fix
title: audit-bot-listener-va-audit-terminal-bir-tokenda-toqnashadi
date: 2026-09-05
status: draft
verified: false
---

2026-09-05 ~13:20. Bekzod (914653833) 'kim audit ga start bosmagan' deb soradi. Tekshirildi: Xodim reestri holati ozgarmagan - sd-xodim-chat.json hali ham bosh (xodimlar={}, arizalar={}). YANGI TOPILDI: sd-listener.mjs (/start qabul qiluvchi jarayon, AUDIT_BOT_TOKEN) 2026-09-04T08:11:07 dan beri olik edi - process yoq, supervisor (sd-listener-supervisor.ps1) ham ishlamayapti, Task Scheduler'da ham yoq. Qayta ishga tushirishga urinildi - 409 Conflict: sd-listener.mjs va channels/telegram-audit (audit-terminal Claude sessiyasining oz Telegram kopригi) IKKALASI HAM bir xil bot token (8754739863, @hoffen_auditbot) bilan getUpdates qiladi - Telegram bitta tokenga bitta long-poll beradi. sd-listenerni qayta ochirib qoydim, aks holda Ruslan/Bekzodning audit sessiya bilan suhbati ham uzilib qolishi mumkin edi. Bekzoddan qaror sorandi: (a) registratsiya uchun alohida bot/token (ombor patterni), yoki (b) /start logikasini audit-terminal koprigining ichiga kochirish. Javob kutilmoqda. status: draft, verified: false.

*<- [[hub|Xarita]]*
