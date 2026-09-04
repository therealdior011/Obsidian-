---
type: fix
title: hisobot-tekshiruv soxta qarz farqi va taxminiy ustun indekslari
date: 2026-09-04
status: draft
verified: false
---

2026-09-04. Ruslan qoidasi (hisobotlarda 1 marotaba ham taxmin bolmasin) boyicha tekshiruv modulining OZIDA 3 ta taxmin topildi va tuzatildi. (1) Savdo yakuni sahifadagi eng katta raqam deb olinardi - endi aynan 'panel-title Obshaya summa' sarlavhasidan olinadi (oddiy matn qidiruvi yaramaydi: sahifa yuqorisida navigatsiya royxatida ham shu soz bor). (2) /clients/transactions/JsonData javobida ustun NOMLARI yoq, kod row[6]=rayon, row[11]=balans deb qattiq yozgan edi - hech qayerda tekshirilmagan. Sahifaning oz JS kodida allColumnNames = before + currencyNames + after ekan, yani ortaga VALYUTA ustunlari qistiriladi va valyuta qoshilsa keyingi hamma ustun surilib ketardi, hisobot esa jimgina notogri raqam berardi. Yangi sd-ustunlar.mjs moduli indeksni NOM boyicha beradi, topilmasa ochiq xato beradi. (3) Qarzdorlik tekshiruvi debtApi jamisini mijoz balanslari bilan solishtirardi va ular teng bolishi kerak deb hisoblardi - bu NOTOGRI, ular ikki boshqa narsani olchaydi. Dalil: mijoz 4062 Zikrillox, Nalichniy -4467000, Beznalichniy +4371000, Obshiy -96000, debtApi 1551000 - uchalasi ham togri, uch xil savolga javob. Bu soxta farq 2026-09-03 da 26 mln qizil qator chiqargan edi. Endi debtApi ozi ichdan tekshiriladi (jami = 0-7..90+ kun guruhlari, 437 mijozda 0 farq), balans esa ALOHIDA korsatkich sifatida valyuta ustunlari yigindisi bilan tekshiriladi. Natija: 7 korsatkich, hammasi mos.

*<- [[hub|Xarita]]*
