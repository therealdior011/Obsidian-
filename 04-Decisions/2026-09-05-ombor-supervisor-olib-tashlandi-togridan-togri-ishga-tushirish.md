---
type: decision
title: ombor-supervisor-olib-tashlandi-togridan-togri-ishga-tushirish
date: 2026-09-05
status: confirmed
verified: false
---

2026-09-05 00:06-00:09 Ruslan talabi: 'supervisor qayta yoqilmasin, omborni fix qil va qayta ishga tushir'. BAJARILDI: (1) ombor-terminal-supervisor.ps1 jarayoni to'xtatildi (PID 3216) va skriptning o'zi .assistant\scripts\_ochirilgan\ombor-terminal-supervisor.ps1.20260905-0006 ga ko'chirildi - endi cheksiz qayta-urish sikli YO'Q. (2) Startup\OmborBotBridge.lnk zaxiraga olindi va YANGI nishonga qayta yo'naltirildi: .assistant\scripts\ombor-terminal-start.bat (oddiy .bat, sikl yo'q, TELEGRAM_STATE_DIR faqat shu jarayon uchun set qilinadi - USER darajasida EMAS). (3) Eski ombor sessiyasi (claude 12788) va uning yetim bun pollerlari (5040, 13708) to'xtatildi. (4) Yangi sessiya ko'tarildi: claude PID 12768 (00:07:40), poller bun 2616 -> telegram-ombor\bot.pid 00:07:43 da yangilangan. getMe -> @hoffen_ombor_managerbot ok=true, pending=0. TEKSHIRILDI: uchala kanal (main 8036 / audit 10848 / ombor 2616) o'z pollerida, yetim bun qolmadi, token to'qnashuvi yo'q. MUHIM: .bat buyrug'ida 'ombor-terminal' so'zi saqlab qolindi - asosiy supervisor belgisiz claude larni o'ldiradi, shu belgi uni chetlab o'tishga majbur qiladi. QOLDI: yangi sessiya haqiqatan Telegram xabariga javob berishi jonli test bilan tasdiqlanmadi - Bekzoddan test xabar so'raldi.

*<- [[hub|Xarita]]*
