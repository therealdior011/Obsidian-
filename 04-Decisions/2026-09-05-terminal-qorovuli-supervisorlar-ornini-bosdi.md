---
type: decision
title: terminal-qorovuli-supervisorlar-ornini-bosdi
date: 2026-09-05
status: confirmed
verified: false
---

2026-09-05 00:10-00:26 Ruslan talabi: 'qo'riqchi qo'y - terminal yopilsa yoki kompyuter o'chib yonsa qaytadan ishga tushsin, 3 ta terminalni qo'lda yoqish azob, va modellar default sonnet 5 bo'lsin'. BAJARILDI. (1) UCHALA SUPERVISOR OLIB TASHLANDI (telegram-listener / ombor-terminal / audit-terminal-supervisor.ps1) - ular cheksiz 'while(true){claude; sleep 10}' siklida ishlardi; supervisorning O'ZI o'lsa hech kim ko'tarmasdi (2026-09-04 da ombor 1s38d o'lik turgan). Skriptlar va eski Startup yorliqlari .assistant\scripts\_ochirilgan\ da (20260905). (2) YANGI: uchta oddiy ishga tushiruvchi .bat - main-terminal-start.bat / ombor-terminal-start.bat / audit-terminal-start.bat. Har biri TELEGRAM_STATE_DIR ni FAQAT o'z jarayoniga beradi, ish papkasiga cd qiladi (CLAUDE.md konteksti o'qilishi uchun) va --model sonnet bilan ishga tushiradi. (3) QO'RIQCHI: scripts\qorovul.ps1 - sikl YO'Q, bir marta ishlaydi va chiqadi: USER darajasidagi TELEGRAM_STATE_DIR qoldig'ini tozalaydi, EGASIZ ko'priklarni (ota-zanjirida tirik claude.exe yo'q bun server.ts) o'ldiradi, keyin 'main-terminal'/'ombor-terminal'/'audit-terminal' belgisi bo'yicha qaysi terminal o'lik bo'lsa Start-Process orqali .bat ni ko'taradi (claude.exe haqiqiy konsol talab qiladi). (4) ISHGA TUSHISH: Task Scheduler 'SD-TerminalQorovul' har 5 daqiqada (Interactive only) + Startup\TerminalQorovul.lnk logon uchun. DIQQAT: /sc ONLOGON vazifasi admin talab qiladi (Access denied) - shuning uchun logon Startup yorlig'i orqali. (5) kanal-qorovul.ps1 ham yangilandi: endi mavjud bo'lmagan supervisorlarni emas, yangi .bat larni chaqiradi. JONLI SINOV (dalil): audit sessiyasi (PID 12632) ataylab o'ldirildi -> qorovul egasiz ko'prikni (10848,4128,8900) tozaladi va audit ni PID 10880 sifatida --model sonnet bilan ko'tardi. Yakuniy holat: main 6652 (hali opus - qayta yoqilganda sonnet bo'ladi), audit 10880 sonnet, ombor 7032 sonnet; ko'priklar main->8036, audit->10476, ombor->8048, yetim yo'q, USER STATE_DIR qoldig'i yo'q.

*<- [[hub|Xarita]]*
