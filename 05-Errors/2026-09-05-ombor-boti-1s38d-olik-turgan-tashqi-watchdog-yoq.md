---
type: fix
title: ombor-boti-1s38d-olik-turgan-tashqi-watchdog-yoq
date: 2026-09-05
status: draft
verified: false
---

2026-09-04 23:00-00:05 Bekzod: 'hoffen ombor boti ishlamayabdi, qayta ishga tushmagan'. TEKSHIRUV (dalil, taxmin emas): ombor supervisor PID 3216 tirik (23:42:55), claude.exe PID 12788 tirik (23:42:56), telegram-ombor\bot.pid=13708 bun tirik (23:43:03), getMe -> @hoffen_ombor_managerbot ok=true, webhook yo'q, pending_update_count=0. Uchala kanal (telegram / telegram-audit / telegram-ombor) HAR BIRI o'z tirik bun polleriga ega -> token to'qnashuvi YO'Q. ASL SABAB: ombor-terminal.out.log bo'yicha sessiya 2026-09-04 22:04:19 da yiqilgan (exit -1) va 23:42:55 gacha ~1 soat 38 daqiqa O'LIK turgan - o'sha oraliqdagi xabarlar javobsiz qolgan. Shu kuni 09:17 da yana ikki marta exit -1073740791 (0xC0000409 stack buffer overrun) bilan yiqilgan. Ya'ni 'qayta ishga tushmagan' emas - KECH ishga tushgan. Supervisor faqat claude.exe o'zi chiqib ketganda 10 soniyada qayta uradi; supervisorning O'ZI o'lsa yoki sessiya osilib qolsa (jarayon tirik, lekin javob bermaydi) hech kim ko'tarmaydi va bu soatlab davom etadi. KEYINGI QADAM (hali BAJARILMADI): tashqi watchdog kerak - SD-Watchdog vazifasiga uchala supervisor (asosiy/audit/ombor) tirikligini va oxirgi javob vaqtini tekshirish qo'shilsin.

*<- [[hub|Xarita]]*
