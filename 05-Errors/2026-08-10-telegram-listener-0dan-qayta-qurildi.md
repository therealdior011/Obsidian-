---
type: fix
title: telegram-listener-0dan-qayta-qurildi
date: 2026-08-10
status: draft
verified: false
---

Ruslan talabi bilan Telegram listener butunlay qayta qurildi. ASOSIY SABAB TOPILDI: telegram-listener.err.log da 'Error: Input must be provided either through stdin or as a prompt argument when using --print' xatosi - Task Scheduler orqali ishga tushirilgan claude.exe haqiqiy konsol/TTY ololmay, avtomatik --print rejimiga o'tib, darhol xato bilan o'chib qolar edi (har 10-13 soniyada qayta-qayta, Last Result -1073741510 = majburiy to'xtatilgan). YECHIM: eski 'ClaudeCode-TelegramListener' Task Scheduler vazifasi butunlay o'chirildi (Unregister-ScheduledTask). O'rniga Windows 'Startup' papkasiga (shell:startup) TelegramListener.lnk shortcut qo'shildi - bu launch-claude.bat kabi HAQIQIY konsol bilan ishga tushadi (aynan hozirgi ishlab turgan sessiya PID 7064 kabi), Task Scheduler'ning TTY muammosidan xoli. Yangi telegram-listener-supervisor.ps1 (eski nusxa .old backup qilindi) da: duplikat-himoya (agar --dangerously-skip-permissions bilan claude.exe allaqachon ishlab tursa - chiqib ketadi), va har chiqishda log yozadi (telegram-listener.out.log). HALI TASDIQLANMAGAN: bu ad-hoc terminal sessiya (PID 7064, hozir Telegram kanalini ushlab turibdi) yopilgandan keyin, Windows qayta yoqilganda yoki telegram-listener-start.bat qo'lda ishga tushirilganda, yangi listener chindan ham soatlab barqaror ishlashini keyingi safar tekshirish kerak. status: draft.

*<- [[hub|Xarita]]*

## 2026-08-10 - qo'shimcha
TASDIQLANDI 09:18: Ruslan Telegram orqali xabar yubordi ('Maslaxatin kerak', chat_id 104766999) va u shu ad-hoc terminal sessiyasi (PID 7064) orqali muvaffaqiyatli qabul qilindi va javob yuborildi (reply tool orqali). Demak: ochiq terminal sessiya + Telegram kanali BIR VAQTDA ishlaydi, muammo faqat sessiya YOPILGANDAN keyin avtomatik qayta ko'tarilmasligida edi (Task Scheduler TTY xatosi). Yangi Startup-papka mexanizmi hali alohida, sessiya yopilgandan keyingi holatda sinalishi kerak (hali qilinmagan).
