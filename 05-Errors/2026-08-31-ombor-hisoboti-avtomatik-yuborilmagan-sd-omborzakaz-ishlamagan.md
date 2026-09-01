---
type: fix
title: ombor-hisoboti-avtomatik-yuborilmagan-sd-omborzakaz-ishlamagan
date: 2026-08-31
status: draft
verified: false
---

2026-08-31 TEKSHIRUV (Ruslan sorovi: "omborxona hisobotlari borganmi, rasm korinishidami"). NATIJA: OMBOR HISOBOTI HECH QACHON AVTOMATIK YUBORILMAGAN. Dalillar: (1) SD-OmborZakaz vazifasi LastRunTime = 30.11.1999, LastTaskResult = 267011 (0x41303 "hali ishlamagan"), NumberOfMissedRuns = 0, NextRunTime 07.09.2026. Trigger togri sozlangan - har dushanba 09:00, StartBoundary 2026-08-30. Birinchi ishlashi bugun 31.08 (dushanba) 09:00 bolishi kerak edi. (2) SABAB: kompyuter 31.08 00:55:17 da uyquga ketgan (Kernel-Power 42) va 17:34:04 da uygongan. 09:00 da mashina ochiq edi. (3) MUAMMO: StartWhenAvailable=true bolsa ham catch-up ISHLAMADI - boshqa vazifalar (SalesDoc-DailyReport, SD-AuditReport, AssistantReindex) 17:40 da otib ketganini qaytarib bajardi, SD-OmborZakaz esa bajarmadi va keyingi ishlashni 07.09 ga surdi. Sababi aniqlanmagan.
FORMAT TOGRI: ombor-rasm.mjs --yubor sendPhoto orqali RASM yuboradi, 4 manzilga (ombor boti->Ruslan, audit boti->Ruslan, audit boti->Bekzod, ombor boti->Bekzod). Ya'ni "hisobot rasm korinishida" qoidasi ombor uchun kodda bajarilgan - lekin kod hech qachon avtomatik ishga tushmagani uchun amalda hech kim rasm olmagan. Qolda yasalgan oxirgi rasm: _rasm-ombor.png, 2026-08-30 19:54.
IKKINCHI KAMCHILIK: bot faqat aniq buyruqni tushunadi. 31.08 18:11 da Bekzod "hisobot ber" deb yozdi - ombor-javob.mjs uni mahsulot qidiruvi deb qabul qildi va "mahsulot topilmadi" javobini berdi. Rasm faqat /zakaz buyrugida keladi. Tabiiy tildagi "hisobot", "zakaz ber", "otchet" kabi soralarni /zakaz ga yonaltirish kerak.
TEKSHIRILDI: ombor-rasm.mjs qolda ishga tushirildi (--yubor siz) - ishlayapti, 58 ta mahsulotga zakaz, 49 tasi asosiy omborda yoq.

*<- [[hub|Xarita]]*
