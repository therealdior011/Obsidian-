---
type: decision
title: dokon-kartochkalari-agentlar-uchun
date: 2026-08-26
status: confirmed
verified: false
---

2026-08-26 03:20 DOKON KARTOCHKALARI QURILDI VA YUBORILDI (Ruslan 'Axa shunaqa qil' dedi). SKRIPT: scratchpad\kartochka.py. MANBA: 4 ta buyurtma fayli (2026-02-19 .. 2026-08-25, yangi 18-26 avgust ham qoshildi) + mijozlar royxati. HAR AGENT UCHUN ALOHIDA FAYL: kartochka\<agent>.txt; ustunlar - DOKON, OXIRGI buyurtma, MARTA (necha marta olgan), ORT.SUMMA, XIL (ortacha nechta turli mahsulot), MAQSAD (ortachadan 40% kop summa + bittadan kop xil); 45+ kun jim dokonlar '<< N kun yoq!' deb belgilangan; royxat summa boyicha tartiblangan. NATIJA (13 fayl): Offis 153 dokon/74 jim; Muhammad Ali 149/53; Murodullayev 142/42; Athamov 131/35; Boxodirxoja 129/61; Muhammadjonov 112/41; Yashnobod&Sergeli 110/73; Angren 109/38; Sobirov 93/30; Sobitov 76/31; Djorayev 65/25. ENG OGIR HOLAT: Yashnobod&Sergeli (110 dan 73 tasi jim = uchdan ikkisi) va Offis (153 dan 74). IKKI TUZOQ TOPILDI VA TUZATILDI: (1) agent maydonida '<br/>' (nafaqat '<br>') - dastlab agentlar 22 ta soxta variantga bolinib ketdi ('Yashnobod & Sergeli<br/>Offis' kabi); yechim - re.split(r'<br\s*/?>') va har bolakdan oxirgi qavs olib tashlanadi; dokon HAR IKKALA agent royxatida chiqadi (ikkalasi ham tashrif buyuradi); (2) 'ortacha DONA' korsatkichi QOGOZ tufayli BUZILGAN - qogoz mingtalab sotiladi, bitta dokonda ortacha 102 dona chiqib taklif 153 ta bolgan (manosiz); yechim - dona olib tashlandi, orniga SUMMA va XIL (turli mahsulot soni) qoyildi, bular buzilmaydi. RUSLANGA YUBORILDI: 11 ta asosiy agent fayli (ikki xabarda) + tushuntirish. TAKLIF QILINDI (javob kutilmoqda): kartochkalarni har hafta avtomatik yangilash, dushanba ertalab ozi ketadigan qilish.

*<- [[hub|Xarita]]*
