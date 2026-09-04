---
type: fix
title: sd-watchdog eskirgan vazifalarni kuzatardi
date: 2026-09-04
status: draft
verified: false
---

2026-09-04. Qorovul (sd-watchdog.ps1) BUTUNLAY eskirgan edi: SalesDoc-DailyReport, SalesDoc-EveningReport, SalesDoc-MonthlyReport nomli vazifalarni va salesdoc-daily-report.log, salesdoc-evening-report.log fayllarini kuzatardi. Ularning hech biri endi mavjud emas - vazifalar SD-* nomlariga otgan, log fayllari hech qachon yozilmagan. Natija: (1) har kuni SOXTA ogohlantirish ketardi (03-sentabr: 4 va 5 muammo, hammasi topilmadi turidagi, aslida hamma hisobot normal ketgan), (2) HAQIQIY ishlaydigan 4 ta hisobot (SD-HisobotKunlik, SD-HisobotDavriy, SD-OmborZakaz, SD-AuditReport) umuman kuzatilmasdi - yani qorovul yopishi kerak bolgan jim buzilish teshigi ochiq turgan. QAYTA YOZILDI: endi faqat haqiqiy dalil tekshiriladi - Task Scheduler LastRunTime bugungi sana bilan mos keladimi, LastTaskResult 0 mi, va natija PNG fayli bugun yangilanganmi. Kechagi sana boyicha sinaldi: 4 tasi ham ishladi=True natija=0 rasm bugungi=True. Yana ikkita saboq: (a) skriptni sinash uchun ishga tushirganimda u haqiqiy Telegram ogohlantirish yubordi - endi -Sinov bayrogi qoshildi; (b) PowerShell 5.1 BOMsiz UTF-8 ni ANSI deb oqiydi, em-dash belgisi parser xatosi berdi - .ps1 fayllar BOM bilan saqlanishi shart. Ochiq zaiflik: hisobot skriptlari log yozmaydi, Task Scheduler stdout ni ushlamaydi, yani xato matni saqlanmaydi. Retry hech qayerda yoq.

*<- [[hub|Xarita]]*
