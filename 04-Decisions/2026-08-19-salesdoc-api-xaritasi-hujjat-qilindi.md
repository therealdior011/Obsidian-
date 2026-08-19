---
type: decision
title: salesdoc-api-xaritasi-hujjat-qilindi
date: 2026-08-19
status: confirmed
verified: false
---

2026-08-19: Ruslan sorovi - 'SalesDoc boyicha nimani qayerdan qaysi API dan olish (MCP) map tuzib ber, kod yoz, localda ishga tushur, korinish va tushunchani tekshir, keyin Telegram guruhga -1004396447152 yubor'. QILINDI: C:\Users\user\Desktop\salesdoc-api-xarita.html - 8 bolim (savdo, qarzdorlik, ombor/prixod, mijozlar, agent intizomi, GPS, rejalar, texnik qoidalar) + 'Oltin qoida' bolimi. Faqat AMALDA tekshirilgan endpointlar kiritildi. LOCALDA TEKSHIRILDI: file:// URL ni Chrome MCP qabul qilmaydi, Playwright brauzeri band edi (boshqa sessiya) - shu sababli python -m http.server 127.0.0.1:8901 kotarilib, Edge --headless=new --screenshot bilan PNG ga render qilindi va rasm kozdan kechirildi. Sahifa toliq (1200x3960), layout buzilmagan, matn oqiladi, ozbekcha va ruscha belgilar togri chiqdi. Server keyin tox tatildi. YUBORISH BAJARILMADI: telegram reply xatosi - 'chat -1004396447152 is not allowlisted'. Guruh allowlistda yoq. MEN OZIM /telegram:access ni ISHGA TUSHIRMADIM - dostup ozgartirish egasining qarori, Ruslanga terminaldan ozi qoshishi aytildi. XARITADAGI ENG QIMMATLI QISM - tortta tuzoq: (1) savdo = sales.summa, closed_amount EMAS (2.3x farq); (2) qarzdorlikda ikki xil raqam - sof balans -437.6 mln va zakaz boyicha qarz 779.5 mln, /dashboard/dolg dan olmaslik; (3) volume hamma joyda kg emas (qogoz = dona); (4) /report/visit/getjson reja satrlarini ham qaytaradi, visited=Poseshennye mezoni kerak.

*<- [[hub|Xarita]]*
