---
type: decision
title: nazorat-qatlami-qurildi-raqamlarni-avtomatik-tekshiradi
date: 2026-08-19
status: confirmed
verified: false
---

2026-08-19 NAZORAT QATLAMI QURILDI VA SINALDI (Ruslan sorovi: 'avtomatik fix qilish va bu uchun prompt yozib otirmasligimning ilojisi bormi'). TAMOYIL AYTILDI VA QABUL QILINDI: tizim OZI TUZATMAYDI (nomalum xatoni kod togri tuzata olmaydi, va ishlab turgan kodni ozi-ozi ozgartirishi xavfli - 2026-08-14 saboqi), lekin OZI ANIQLAYDI va TOXTATADI. 'Xato raqam bilan hisobot kelgandan kora, hisobot kelmagani yaxshi.' Ruslandan prompt talab qilinmaydi - hammasi kod, jadval boyicha. FAYL: sd-nazorat.mjs, eksport: tekshir(d, from, to). UCHTA TEKSHIRUV: (1) SAVDO - mening hisobim (orders/list/orders -> sales.summa) SalesDoc'ning OZ hisoboti (/report/agent) bilan solishtiriladi, 1% dan katta farq = XATO; (2) QARZDORLIK - arifmetik nazorat 11-ustun = 12+13+16, buzilsa = XATO (tuzilma ozgarsa yoki notogri ustun olinsa darhol bilinadi); (3) MANTIQIY - savdo manfiy emasmi, buyurtma bor-u savdo 0 emasmi, mijoz soni buyurtmadan kop emasmi, 200% dan katta sakrash bormi. SINOV NATIJASI (ataylab bugungi xatolar takrorlandi): eski xato usul (closed_amount) 156,061,500 vs mustaqil 385,646,500 = 147.1% farq -> TOXTATILADI (USHLADI!); togri usul (sales.summa) 386,146,500 = 0.1% farq -> OK; qarzdorlik arifmetikasi joyida, agar 12-ustun olinsa (-555,533,929) arifmetika buziladi -> TOXTATILADI. ULANDI: sd-growth.mjs --send rejimida hisobot yuborishdan OLDIN tekshir() chaqiradi; xato bolsa hisobot YUBORILMAYDI, ornига Ruslanga ogohlantirish ketadi va sd-growth.log ga yoziladi, exit kod 2. Eksport tekshirildi - import ishlaydi.

*<- [[hub|Xarita]]*
