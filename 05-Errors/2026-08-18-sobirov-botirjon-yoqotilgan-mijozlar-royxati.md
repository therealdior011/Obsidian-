---
type: fix
title: sobirov-botirjon-yoqotilgan-mijozlar-royxati
date: 2026-08-18
status: draft
verified: false
---

2026-08-18 ~05:10 Ruslan Telegram orqali soradi: 'Sobirov Botir hududida oldin maxsulot xarid qilib keyin xarid qilmay qoygan xaridorlar royxatini tashab ber'. USUL (08-11dagi Boxodirxoja tahlili bilan bir xil, lekin toliqroq - 6 oy, faqat 2 oy emas): /orders/list/orders har oy uchun (mart-avgust 2026) alohida sorаldi, agent_id=d0_95 (Sobirov Botirjon) boyicha filtrlanib, noyob client_id lar yigildi. TEXNIK TOPILMA: MCP get_dashboard_page orqali 1 oylik /orders/list/orders 1.1MB - token limitidan oshadi. Togridan-togri fetch bilan olinganda esa javob {data:{orders:...}} EMAS, TOGRIDAN-TOGRI {orders:[...], sales:[...], bonuses:...} - MCP serverining ozi 'data' oramini qoshar ekan (avvalgi sd-metrics.mjs topilmasi bilan bir xil naqsh - MCP serverlari xom javobni ozgartiradi). Konnektsiya vaqti-vaqti bilan uzilib qoladi (ConnectTimeoutError) - 3 marta qayta urinish qoshildi, ishladi. NATIJA: mart-iyun oylarida Sobirovdan xarid qilgan 85 ta noyob mijoz, iyul VA avgustning IKKALASIDA HAM yoq bolgani 21 ta. MUHIM GEOGRAFIK TOPILMA: 21 tadan 16 tasi (76%) BITTA HUDUDDA - Toshkent Tumani (qolgani Zangi Ota 4, Yashnaobod 1) - bu Boxodirxoja tahlilidagi (16-avgust, Qibray/Chirchiq korridori) bilan BIR XIL NAQSH, tasodifiy emasligini kuchaytiradi. Oxirgi buyurtma oyi taqsimoti: Mart-5, Aprel-1, May-9, Iyun-6 - asosiy chiqib ketish MAY-IYUNDA (15/21), mart emas (08-11dagi Boxodirxoja tahlilida ham xuddi shunday saboq bor edi - 'oxirgi oy taxmin qilinmasin, har doim tekshirilsin'). Toliq royxat (ism, telefon, hudud, buyurtma soni) Telegramga yuborildi. 2 ta mijozda telefon raqami tizimda yoq. Skript: C:\Users\user\.assistant\sd-pipe\_sobirov.mjs (vaqtinchalik, keyinchalik boshqa agentlar uchun qayta ishlatilishi mumkin - AGENT_ID ozgartirish yetarli).

*<- [[hub|Xarita]]*
