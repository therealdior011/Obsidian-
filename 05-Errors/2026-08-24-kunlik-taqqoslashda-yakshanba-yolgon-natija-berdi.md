---
type: fix
title: kunlik-taqqoslashda-yakshanba-yolgon-natija-berdi
date: 2026-08-24
status: draft
verified: false
---

2026-08-24 22:40 JIDDIY XATO TOPILDI VA TUZATILDI (Bekzod 'rasm qanday korinishda bormoqda menga yubor' degani sababli namuna yasayotganimda TASODIFAN chiqdi). XATO: kunlik izoh 'Savdo 23,939,000 -> 780,000 (-96.7%)' deb chiqdi. SABAB: 23-avgust YAKSHANBA edi, osha kuni atigi 1 ta buyurtma bolgan; sd-growth.mjs da 'ish kuni' filtri bor edi (2026-08-18 da qoshilgan) lekin u 'k.buyurtma > 0' deb tekshirardi - 1 ta buyurtma ham 0 dan kop, shuning uchun yakshanba ISH KUNI deb qabul qilingan va 52 buyurtmali shanba bilan solishtirilgan. OQIBAT (agar toxtatilmasa): hisobot guruhga 'savdo 97% tushdi' deb chiqardi, Ruslan va jamoa keraksiz vahimaga tushardi. TUZATISH: sd-growth.mjs ga ISH_KUNI_ENG_KAM = 10 ostonasi qoshildi, sharti 'k.buyurtma >= ISH_KUNI_ENG_KAM' ga ozgartirildi; kodda toliq izoh qoldirildi. TEKSHIRUV: tuzatishdan keyin taqqoslash togri chiqdi - 22-avgust vs 21-avgust, savdo 21,173,000 -> 23,939,000 (+13.1%), buyurtma 43->52, xaridor 40->47, chek 492,395->460,365 (-6.5%). SABOQ: 2026-08-18 dagi tuzatish YETARLI EMAS edi - 'noldan katta' sharti dam olish/bayram kunlarida 1-2 ta tasodifiy buyurtma bolganda ishlamaydi; ostona QIYMAT bilan qoyilishi kerak edi. UMUMIY SABOQ: namuna yasash/korsatish sorovi ozi TEKSHIRUV vazifasini bajardi - agar Bekzod soramaganda bu xato kechqurun avtomatik hisobotda guruhga chiqib ketardi. BEKZODGA HAMMASI OCHIQ AYTILDI (rasm + izoh + topilgan xato).

*<- [[hub|Xarita]]*
