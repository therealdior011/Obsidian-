---
type: error
title: salesdoc-litsenziyasi-tugadi-nima-ishlaydi
date: 2026-09-01
status: confirmed
verified: false
---

2026-09-01 06:xx LITSENZIYA TUGADI - TASDIQLANDI (taxmin emas, sahifa ochib ko'rildi). /stock/stock/detail va boshqa HTML sahifalar 'Sales Doctor - Billing' ga yo'naltirilyapti. ISHLAMAYDI: /stock/stock/detail (ombor qoldiqlari), /finans/pnl, /report/workingTime, /product/* - hamma HTML hisobot sahifalari. HALI ISHLAYDI: /orders/list/orders (JSON), /warehouse/list/data (JSON), POST /clients/client/JasonData2 (JSON). Ya'ni JSON endpointlar ochiq, HTML sahifalar yopiq. TA'SIRI: ombor agenti (ombor-qoldiq.mjs) TO'XTADI. Kunlik hisobot ISHLAYDI. CHORA KO'RILDI: mahsulot-lugat.mjs yaratildi - mahsulot id->nom lug'ati _mahsulot-lugat.json da doimiy saqlanadi (222 ta nom, 30-avgustdagi saqlangan stock.html nusxasidan ajratildi). Litsenziya tiklangach 'node mahsulot-lugat.mjs --yangila'. Shu tufayli kunlik hisobot mahsulot nomlarini litsenziyasiz ham ko'rsatadi. Ruslanga 4-marta ogohlantirish yuborildi (msg 370127).

*<- [[hub|Xarita]]*
