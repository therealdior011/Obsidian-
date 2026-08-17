---
type: fix
title: salesdoc-prixod-kg-hisoblash-usuli
date: 2026-08-17
status: draft
verified: false
---

2026-08-17 IYUL SUXOY TUMAN - TASDIQLANGAN USUL BILAN QAYTA HISOBLANDI VA RUSLANGA TOGRILANDI. XATOM: avval kg ni mahsulot NOMIDAN parse qilishga urindim (masalan '1 Kg' matnidan) - bu TUZOQ, tizimda alohida 'volume' maydoni bor ekan, shu ishlatilishi kerak (bu xotirada ilgari - ehtimol parallel sessiyada - topilgan va tasdiqlangan usul edi). TOGRI YOL: (1) POST /stock/planProduct/getProducts -> {data:[{text,value}]} - mahsulot lugati, 'text'=nom 'value'=product_id. (2) POST /stock/purchaseReportPivot/pivotData?date=YYYY-MM-DD,YYYY-MM-DD -> MASSIV (dict emas), 0-qator SARLAVHA: product_cat,product,count,summa,price,volume,block,time,created,shipper. 'product' = product_id (nom emas, lugat bilan bogash kerak), 'volume' = KG (togridan-togri, parse kerak emas). IYUL NATIJASI (togrilangan): 01.07=117kg, 10.07=14kg, 11.07=11kg, 16.07=3kg, 18.07=1.5kg, 27.07=4kg, 30.07=44.5kg, 31.07=5kg. JAMI: 227 dona, 200 kg, 28,560,000 som (avvalgi notogri hisobim: 231 dona, 'kg noaniq' degan edim - bu BEKOR QILINDI, Ruslanga aytildi). TUZOQ: 2 ta qatorda (MOLECULES 01, BLACK AFGANO, ikkalasi 1kg lik, narxi 140000) tizimda volume=0 korsatilgan - bu tizimning oz xatosi, narxdan 1kg ekani aniq, qoshilsa jami ~202 kg. Ruslan aytgan fakt (faqat 0.5kg va 1kg qadoq) tizimda TASDIQLANDI. SABOQ: manba tanlash togri bolsa ham, BIR MAYDONNI IKKI XIL USULDA UQISH MUMKIN (nomdan taxmin vs alohida maydon) - aynan CLAUDE.md dagi 4-qonun holati, ikkalasini solishtirmasdan biriga ishonib bolmaydi.

*<- [[hub|Xarita]]*
