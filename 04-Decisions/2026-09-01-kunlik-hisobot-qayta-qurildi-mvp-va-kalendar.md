---
type: decision
title: kunlik-hisobot-qayta-qurildi-mvp-va-kalendar
date: 2026-09-01
status: confirmed
verified: false
---

2026-09-01 RUSLAN TOPSHIRIGI BAJARILDI. MUAMMO: (1) 22:00 dagi 'kunlik' hisobot oxirgi IKKI ISH KUNINI solishtirardi (kecha vs undan oldingi), Ruslan sana bilan chalkashardi; (2) haftalik/oylik/yillik HAR KUNI 22:05/22:10/22:15 da guruhga ketardi - har oqshom 4 ta rasm, 3 tasi ma'nosiz. YANGI TIZIM: hisobot-kunlik.mjs (ma'lumot) + hisobot-kunlik-rasm.mjs (2 rasm + yuborish + Obsidian) + hisobot-davriy.mjs (kalendar dispetcheri). Vazifalar: SD-HisobotKunlik 22:00, SD-HisobotDavriy 22:05. O'CHIRILDI (o'chirib tashlanmadi, qaytarish mumkin): SD-GrowthKunlik/Haftalik/Oylik/Yillik. KALENDAR: yakshanba->haftalik, oyning oxirgi kuni->oylik, 31-dekabr->yillik. Windows vazifa rejalashtiruvchisi 'oyning oxirgi kuni' triggerini bermaydi (fevral 28/29), shuning uchun kalendar KODDA tekshiriladi. Sinovdan o'tdi: 2027-02-28 yakshanba+oy oxiri -> ikkalasi, 2026-12-31 -> oylik+yillik. MVP FORMULASI (ochiq, rasmda yozilgan): savdo 45%, buyurtma 25%, yangi do'kon 15%, o'rtacha chek 15% - har biri o'sha kunning eng yaxshisiga nisbatan. Faqat savdo bo'yicha tanlansa eng katta hududdagi agent doim yutadi. 'Demo'/'Offis' hisobi MVP dan CHIQARILDI (asosiy ombordan ofis savdosi), lekin umumiy summaga kiradi. YANGI DO'KON TA'RIFI: SalesDoc dagi dataRegistered maydoni BO'SH (2268 mijozda 1970-01-01), shuning uchun yangi do'kon = BUGUN BIRINCHI MARTA XARID QILGAN. Tarix _hisobot-mijoz-tarix.json da (12 oydan urug'lantirildi). OBSIDIAN: 02-Knowledge/kunlik-savdo-tarixi.md jadvali + 06-Daily/<sana>.md.

*<- [[hub|Xarita]]*
