---
type: decision
title: salesdoc-kun-yakuni-avtomatikasi-23-00
date: 2026-08-21
status: confirmed
verified: false
---

2026-08-21 17:45 KUN YAKUNI AVTOMATIKASI QURILDI VA ISHGA TUSHIRILDI (Habibulloh sorovi: kunlik atchot osha kuni kechasi soat 23 da Ruslanga ketsin, sarlavhada '21-avgust tugadi' kabi). YARATILGAN FAYLLAR: (1) sd-pipe\sd-reyting.mjs - SalesDoc ga ozi login qiladi (kredensiallar C:\Users\user\.claude\mcp-servers\salesdoc\.env dan), berilgan sana uchun /orders/list/orders ni oladi, sales.summa boyicha agent reytingini hisoblaydi (closed_amount EMAS), _reyting-shablon.html ga joylab _rasm-reyting.html yasaydi; (2) sd-pipe\_reyting-shablon.html - orin almashtiriladigan shablon ({{SANA}}, {{SUMMA}}, {{BUYURTMA}}, {{AKB}}, {{CHEK}}, {{SATRLAR}}, {{YETAKCHI}}, {{ULUSH}}); (3) sd-pipe\_rasm-faqat.mjs - osish hisobotini yasaydi lekin YUBORMAYDI; (4) scripts\salesdoc-kun-yakuni.ps1 - hammasini birlashtiradi: reyting + kunlik osish rasmlarini yasab OWNER_CHAT_ID ga (Ruslanning shaxsiy chati) yuboradi, xato bolsa Ruslanga xabar beradi, kun-yakuni.log ga yozadi. VAZIFA: Task Scheduler 'SalesDoc-KunYakuni', har kuni 23:00, State=Ready, keyingi 21.08 23:00. TASDIQ: 20-avgust hisoboti bilan jonli sinaldi, 2 ta rasm Ruslanga YETIB BORDI. TEKSHIRUV: sd-reyting.mjs 20-avgust uchun summa=20,648,000, buyurtma=57, AKB=56, chek=362,246 - qolda hisoblaganim bilan AYNAN bir xil. YOL-YOLAKAY 3 TA TUZOQ TOPILDI VA TUZATILDI: (a) Edge headless har safar stderr ga 'task_manager fallback' ogohlantirishi yozadi - ErrorActionPreference='Stop' bilan bu YOLGON XATO bolib skriptni toxtatadi, shu joyda vaqtincha 'Continue' ga otkaziladi; (b) Windows PowerShell 5.1 da Invoke-RestMethod -Form YOQ (PS7+ da paydo bolgan) - multipart yuborish curl.exe orqali qilindi; (c) ozbekcha izoh Telegram tomonidan rad etildi ('strings must be encoded in UTF-8') chunki konsol kodlashi UTF-8 emas - izoh UTF-8 BOMsiz vaqtinchalik faylga yozilib curl ga '-F caption=<fayl' bilan uzatiladi. TEGILMAGAN: 22:00 EveningReport va 22:30 MonthlyReport guruhga (AUDIT_GROUP_ID) ketishda davom etadi.

*<- [[hub|Xarita]]*
