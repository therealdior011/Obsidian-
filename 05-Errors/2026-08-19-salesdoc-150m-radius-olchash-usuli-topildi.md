---
type: fix
title: salesdoc-150m-radius-olchash-usuli-topildi
date: 2026-08-19
status: draft
verified: false
---

2026-08-19 TOPILDI: 150m radius buzilishini o'lchash mumkin ekan - avvalgi hisobotlarda 'aniqlay olmadim' deyilgan edi. USUL: /gps2/monitoring/fetchData?date=YYYY-MM-DD HH:MM:SS endpointi berilgan ONDAGI tarixiy GPS nuqtani qaytaradi (faqat oxirgi nuqtani emas). Har tashrifning start vaqti bilan chaqirib, agent nuqtasini mijoz kartochkasidagi lat/lon (POST /clients/client/JasonData2) bilan solishtirish mumkin. NATIJA 18.08: GPS 5 daqiqadan yangi bo'lgan 253 tashrifdan 59 tasi (23%) mijozdan 150m dan uzoqda; shundan 9 tasi buyurtmali, 3 971 000 som. Konservativ kesim (GPS 2 daqiqadan yangi): 231 dan 41 tasi (18%). MUHIM CHEKLOV: GPS nuqta yoshini albatta filtrlash kerak (15 daqiqa eski nuqta bilan hisoblansa 68 ta chiqadi - shishirilgan raqam); mijoz kartochkasidagi koordinata xato bo'lsa ham buzilish ko'rinadi - bu KUCHLI BELGI, dalil emas. Skript: C:\Users\user\.assistant\sd-pipe\_tb.mjs, xom natija _radius-18.json.

*<- [[hub|Xarita]]*
