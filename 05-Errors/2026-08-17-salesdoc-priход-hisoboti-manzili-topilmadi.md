---
type: fix
title: salesdoc-priход-hisoboti-manzili-topilmadi
date: 2026-08-17
status: draft
verified: false
---

2026-08-17 MANZIL TOPILDI - 12-avgustdagi ochiq muammo YOPILDI. TOGRI ENDPOINT: GET /warehouse/list/purchase?from=YYYY-MM-DD&to=YYYY-MM-DD&by=date (bu API xaritasida bor edi, lekin 12-avgustda sinalmagan - oshanda /warehouse/list/receipt, /arrival, /prihod, /stock/list/receipt sinalgan va hammasi 404 bergan). JAVOB TUZILISHI: {status, result:{purchases:[...], details:[...]}} - IKKALASI HAM birinchi qatori USTUN NOMLARI bolgan massiv. purchases: id, price_type_id, date, warehouse_id, supplier_id, create_at, create_by. details: id, purchase_id, product_id, count, summa, mfg_date, exp_date. Ularni purchase_id orqali bogash kerak. MAHSULOT LUGATI: POST /stock/planProduct/getProducts -> {data:[{text, value}]} - 222 ta mahsulot, 'text' = nom, 'value' = product_id (d0_XX). DIQQAT: maydon nomlari 'name'/'id' EMAS, 'text'/'value'. Sinalgan boshqa nomzodlar: /warehouse/list/product, /warehouse/list/products, /stock/list/product(s), /warehouse/list/purchase-product - hammasi 404. Ishlaganlari: /warehouse/list/data (omborlar), /stock/lotReport/data. NATIJA (iyul 2026, 'сухой туман'): 90 xil mahsulot nomi mos keldi, 59 ta prixod yozuvi, 8 kunda: 01.07 117 dona 16,380,000; 10.07 18 dona 1,960,000; 11.07 16 dona 1,820,000; 16.07 3 dona 420,000; 18.07 3 dona 210,000; 27.07 8 dona 1,120,000; 30.07 61 dona 6,510,000; 31.07 5 dona 700,000. JAMI 231 dona, 29,120,000 som. MUHIM CHEKLOV (Ruslanga aytildi): 231 DONA ni KG deb olish MUMKIN EMAS - olchamlar aralash: 1 kg lik 81 dona, 0.5 lik 46 dona, olchami nomda YOZILMAGAN 104 dona. Aniq hisoblanadigani ~104 kg, qolgani nomalum. HOLAT: Ruslan 'bu malumot notogri' dedi (08:49) - lekin qaysi hisobot ekani aniq emas (osha payt unga 3 xil narsa ketgan: 05:25 audit, 09:10 kunlik SalesDoc, prixod javobi). Aniqlashtirish soraldi, javob kutilmoqda. TAXMIN QILMASDAN kutish kerak.

*<- [[hub|Xarita]]*
