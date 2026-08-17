---
type: fix
title: salesdoc-mahsulot-kartochkalarida-ogirlik-kiritilmagan
date: 2026-08-17
status: draft
verified: false
---

2026-08-17 HAQIQIY MUAMMO TOPILDI (Ruslan 'senga nega 28 560 000 chiqvotdi' deb surishtirgach). MOHIYAT: SalesDoc'da bir qancha mahsulot kartochkasida QADOQ OGIRLIGI kiritilmagan (volume=0), garchi narx togri bolsa ham. Natijada PUL otadi, KILOGRAMM otmaydi - kg va som bir-biriga mos kelmaydi. DALIL (SalesDoc'ning OZ hisoboti, /stock/purchaseReport?from=2026-08-01&to=2026-08-17&by=date, kategoriya 'HOFFEN1 (jidkost suxoy tuman)'): 193 dona / 137 kg / 20 720 000 som. Tekshiruv: 20 720 000 / 140 000 = 148 kg. Tizim 137 kg deb korsatadi. FARQ 11 kg. Matematika: x dona 1kg (140k) + y dona 0.5kg (70k), x+y=193, 140000x+70000y=20720000 -> x=103, y=90 -> haqiqiy 148 kg. Ogirligi 0 turgan mahsulotlar: d0_236, d0_234, d0_237, d0_238, d0_239, d0_241, d0_243. RUSLAN HOLATI: 28 560 000 / 140 000 = 204 kg, u 200 kg olganman deydi -> 4 kg ortiqcha (yo qadoq ogirligi notogri, yo dona soni 204 kiritilgan). Bu raqam 1-17 avgust malumotida YOQ - Ruslandan qaysi sahifa/kun ekani soraldi. MENING HISOBIM TASDIQLANDI: SalesDoc hisobotining kategoriya jamlari (avtoshampun 7635 + trigger 115 + osvejitel 110 + antifriz 3474 + suxoy tuman 137 + nezamerzayka 53 + vosk 1705) = 13 229 kg, men 13 227.45 chiqargandim - farq ~1.5 kg (yaxlitlash). Yani USUL TOGRI, lekin MANBA MALUMOTI NOTOLIQ. TAVSIYA RUSLANGA: ogirligi 0 turgan mahsulotlar royxatini chiqarib, kartochkalarni tuzatish - aks holda farq har oy takrorlanadi.

*<- [[hub|Xarita]]*

## 2026-08-17 - qo'shimcha
2026-08-17 ANIQ ROYXAT TOPILDI (Ruslan 'aynan qaysi maxsulotning kg si korsatilmagan' deb soradi). 1-17 avgustda kirim bolgan, lekin kartochkasida ogirlik maydoni BOSH bolgan suxoy tuman mahsulotlari - 7 ta: (1) MOLECULES 01, 1 kg, 2 dona, 280 000 som; (2) LOUIS VUITTON, 1 kg, 3 dona, 420 000; (3) LOUIS VUITTON, 0.5 kg, 5 dona, 350 000; (4) BLACK AFGANO, 0.5 kg, 2 dona, 140 000; (5) MOLECULES 01, 0.5 kg, 1 dona, 70 000; (6) GIORGIO ARMANI, 0.5 kg, 1 dona, 70 000; (7) GINGER TONIC, 0.5 kg, 4 dona, 280 000. Jami 18 dona, 1 610 000 som. Yigindi ogirlik: 2+3+2.5+1+0.5+0.5+2 = 11.5 kg - men oldin bashorat qilgan 11 kg farqning AYNAN OZI, yani sabab TOLIQ TASDIQLANDI. Nomida '1 Kg'/'0.5 Kg' yozilgan, lekin ogirlik maydoni toldirilmagan. TOPISH USULI: GET /stock/purchaseReport?from=&to=&by=date -> tables[0].rows, ustunlar BITTA ONGGA SURILGAN (Sht.=nom, Obyom=dona, Sena=kg, Summa=narx, 'Data poslednego zakupa'=jami). Shart: dona>0 VA kg=0. CHEKLOV RUSLANGA AYTILDI: bu royxat faqat 1-17 avgustda harakat bolgan mahsulotlar boyicha; bazada boshqa mahsulotlarda ham ogirlik bosh bolishi mumkin, tolq tekshiruv taklif qilindi (javob kelmadi).
