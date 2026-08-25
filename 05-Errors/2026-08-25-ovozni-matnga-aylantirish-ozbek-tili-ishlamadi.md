---
type: fix
title: ovozni-matnga-aylantirish-ozbek-tili-ishlamadi
date: 2026-08-25
status: draft
verified: false
---

2026-08-25 09:30 OVOZNI MATNGA AYLANTIRISH - YOL ISHLAMADI, HALOL YAKUN BERILDI. HOLAT: faster-whisper venv ga ornatilgan (2026-08-21), 'small' model ishlaydi lekin OZBEK TILINI UDDALAY OLMAYDI - chiqqan matn tushunarsiz ('So du kon che yem yodemi abiyomde...'). Kattaroq large-v3 modeli yuklanmoqchi bolindi. MUAMMO: internet SEKIN - 10 daqiqada ~100 MB; model ~3 GB; hozircha 2.3 GB yuklandi (diskda joy egallab turibdi); tugashiga bir necha soat kerak va natija kafolati yoq. Fon rejimidagi ikkita urinish 'killed' boldi (background task cheklovi), ikkita oldingi rejimdagi urinish (580s) atigi 100-200 MB qoshdi. RUSLANGA OCHIQ AYTILDI va SORALDI: yuklashni davom ettiraymi yoki toxtatib yuklanganini ochiraymi (javob kutilmoqda). MUQOBIL YOLLAR TAKLIF QILINDI: (1) Telegram Premium ning oz transkripsiyasi - xabarni bosib 'transcribe' qilib matnni menga tashlash; (2) oddiygina yozib yuborish. TAVSIYAM: muhim narsalarni YOZIB yuborish, ovozni internet yaxshi paytda hal qilish; sabab - ovozni ishonchli oqiy olmasam javobim ham ishonchsiz boladi, bugungidek 'mavzuni togri topdim' holati har doim bolavermaydi. TEXNIK OZGARISHLAR: scripts\ovoz-matn.py - chiqish endi UTF-8 faylga yoziladi (ovoz-natija.txt), konsol cp1251 muammosi hal; model nomi OVOZ_MODEL muhit ozgaruvchisi orqali sozlanadi (kodni ozgartirish shart emas). SABOQ: 'ovozni eshita olmayman' degan cheklovni bir marta aytib qoyish yetarli emas edi - yechim qurishga urinib, uning ham ishlamasligini olchab korish kerak boldi; endi aniq: bu kompyuterda va bu internetda mahalliy ASR ozbek tili uchun amaliy emas.

*<- [[hub|Xarita]]*
