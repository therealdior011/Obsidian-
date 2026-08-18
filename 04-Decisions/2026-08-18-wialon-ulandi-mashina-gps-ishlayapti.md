---
type: decision
title: wialon-ulandi-mashina-gps-ishlayapti
date: 2026-08-18
status: confirmed
verified: false
---

2026-08-18 WIALON MUVAFFAQIYATLI ULANDI. USUL (xavfsiz, parolsiz): Ruslan Token Manager topa olmadi va Playwright bilan parolni ilib olishni taklif qildi - RAD ETILDI. Ornига rasmiy OAuth oqimi ishlatildi: men Playwright bilan https://3.wialon.uz/login.html?client_id=Hoffen-Audit&access_type=256&duration=0&flags=1&response_type=token&lang=ru sahifasini OCHDIM, Ruslan OZI oz login/parolini Wialon'ning OZ sahifasiga kiritdi, men parolga TEGMADIM, redirect URL dan faqat access_token olindi. Sahifa 'Hoffen-Audit poluchit sleduyushchiy uroven dostupa' deb tasdiq soradi - haqiqiy OAuth. MENING XATOM VA TUZATISH: birinchi urinishda access_type=1 qoydim - bu juda TOR edi, core/search_items ishladi lekin messages/load_interval 'error 7' (ruxsat yetarli emas) berdi. Hujjatdan togri qiymat topildi: 0x100 = 256 ('Online tracking' - unga ham asosiy xossalar, ham xabar/tarix oqish kiradi). Ruslan ikkinchi marta kiritdi, token yangilandi. YARATILDI: C:\Users\user\.assistant\sd-pipe\wialon.mjs - login() (token/login), mashinalar() (core/search_items flags:1025), trek() (messages/load_interval). MUHIM TEXNIK ESLATMA: Wialon'da x=LONGITUDE, y=LATITUDE (teskari nomlanish), kodda hisobga olingan. Xato {error:N} shaklida HTTP 200 bilan qaytadi - alohida tekshiriladi. JONLI SINOV NATIJALARI: 10 ta DAMAS topildi (41664 154ZMA, 41663 197RMA, 41668 361TMA, 56043 449HLA, 38650 486QKA, 41665 574VKA, 56070 612EHA, 56042 646ZLA, 41666 970CMA, 56069 998ZMA), HAMMASINING signali 3-13 DAQIQALIK (telefon GPS'ida bazilari 5-14 SOATLIK eski edi - Wialon ANCHA ISHONCHLI), tezliklar real (60, 38, 17 km/s harakatda). TREK SINOVI: unit 41668 uchun bugungi kun - 1373 NUQTA, har ~2 daqiqada, koordinata+tezlik bilan. Bu SalesDoc telefon GPS'idan tubdan yaxshi (u faqat OXIRGI nuqtani berardi). KEYINGI QADAM: sd-store-watch.mjs mantigi (dokon 100m radiusi) Wialon trekiga ulanishi kerak, va mashina<->agent moslashuvi aniqlanishi kerak (DAMAS raqami qaysi agentga tegishli - hali NOMALUM, Ruslandan sorash yoki SalesDoc bilan solishtirish kerak).

*<- [[hub|Xarita]]*
