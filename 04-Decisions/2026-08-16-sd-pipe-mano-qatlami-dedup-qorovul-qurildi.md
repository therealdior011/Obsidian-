---
type: decision
title: sd-pipe-mano-qatlami-dedup-qorovul-qurildi
date: 2026-08-16
status: confirmed
verified: false
---

2026-08-16 ~20:00 QURILDI VA JONLI SINALDI (Ruslan roziligi bilan). Papka: C:\Users\user\.assistant\sd-pipe\. TORT QISM: (1) sd-metrics.mjs - 2-QATLAM MANO QATLAMI. SalesDoc'ga OZI ulanadi (salesdoc MCP serverining .env va login mantigi qayta ishlatilgan, kalitlar nusxalanmagan), /report/visit/getjson va /gps/backend/last dan xom malumot olib, metrikalarni KOD bilan hisoblaydi - LLM umuman qatnashmaydi. MUHIM TEXNIK TOPILMA: xom javob TOGRIDAN-TOGRI massiv, MCP serveri {url,status,contentType,data} oramini OZI qoshar ekan - shu sabab avval xato berdi, tuzatildi. Tuzoqlar kodda: TUZOQLAR.ORDER_SUMMA_FIELD='closed_amount', AGENT_EMAS=[Offis, Yashnobod & Sergeli, Angren & Oqqorgon]. (2) sd-run.mjs - 3-QATLAM QAROR: chegaralar (QISQA_OGISH 0.15 ADAPTIV - guruh medianasidan ogish, statik emas; GPS_ESKI_SOAT 4; BATAREYA_PAST 15; DEDUP_KUN 3; KUNLIK_LIMIT 10), holat fayliga yozadi, dedup qollaydi, toza JSON chiqaradi. (3) sd-state.jsonl - kunlik suratlar, TREND SHUNDAN OQILADI (qidirilmaydi). (4) sd-alerts.json - dedup tarixi. (5) sd-watchdog.ps1 + Task Scheduler 'SD-Watchdog' (10:00 va 23:00, batareyada ishlaydi) - hisobot logida bugungi yozuv yoqmi tekshiradi, vazifalar yoqilganmi, VA batareya cheklovi qaytib kelmaganmi (08-16 ildiz sababi qaytmasin) - muammo topsa Telegram Bot API orqali TOGRIDAN-TOGRI Ruslanga yozadi (Claude sessiyasiga bogliq emas). JONLI SINOV NATIJALARI (hammasi haqiqiy): sd-metrics ishladi - guruh median qisqa-tashrif ulushi 0.493, Abdullaxojaev Boxodirxoja 0.82 (median tashrif 13 SEKUND!), guruhdan ogish +0.327 - keskin ajralib turadi. GPS: 11 dan faqat 2 tasi sogtlom. sd-run 9 ta ogohlantirish chiqardi, ikkinchi ishga tushirishda DEDUP ISHLADI - 9 tasi ham tinch qoldirildi. sd-watchdog ishga tushirildi - ertalabki hisobot yoqligini TOPDI va Ruslanga haqiqiy Telegram xabar YUBORDI (log: '19:59:12 - OGOHLANTIRISH yuborildi: 1 muammo'). Yani 'jim buzilish' muammosi endi yopilgan.

*<- [[hub|Xarita]]*
