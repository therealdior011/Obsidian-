---
type: knowledge
title: salesdoc-agent-nazorati-uchun-real-malumot-tekshirildi
date: 2026-08-16
status: confirmed
verified: false
---

2026-08-16 ~19:10 JONLI TEKSHIRILDI (webdevelopertk savoli boyicha: 'salesdoctordan nima ola olasan'). Ikki manba real chaqirildi, natija DALIL: (1) /report/visit/getjson - 3026 yozuv, 09-16 avgust (8 kun), 11 agent. 16 ta maydon: agent, clientId, client, catclient, city, clientInn, clientChannel, date, start, end, summa, visited (Посещенные), planed (Плановые/Внеплановые), order (Заказ/Нет заказа), reject, photo. DIQQAT: javob JSON dict {url,status,contentType,data}, data[0] = SCHEMA qatori (caption/type), data[1..] = MASSIV (dict emas!) - qiymatlarni keys indeksi orqali olish kerak. Hajmi ~1.1 mln belgi, tool limitidan oshadi - faylga tushadi, python bilan parse qilish kerak. (2) /gps/backend/last?c_datetime=YYYY-MM-DD HH:MM:SS - har agent uchun OXIRGI signal, 19 maydon: AGENT_FIO, AGENT_ID, LAT, LON, TYPE (track/current/sync), BATTERY, SIGNAL, PROVIDER, MODE, GPS_STATUS, INTERNET_STATUS, DEVICE (telefon modeli), DATE, MOB_TIMESTAMP, ORDER_ID, CLIENT_ID, VISIT_ID. MUHIM REAL TOPILMA: bir necha agentda LAT/LON = 0.000000 (Athamov Faxriddin, Muhammadjonov Muhtorjon) - koordinata umuman yoq, GPS ochirilgan yoki fix yoq; Sobitov Abdurahmon batareya 2%, Offis oxirgi signal 14.08 (2 kunlik). Yani GPS nazorati hozir TOLIQ ISHLAMAYAPTI - bu ozi alohida muammo. 8 kunlik tashrif soni: Offis 706, Muhammad Ali 307, Yashnobod&Sergeli 303, Muhammadjonov 270, Athamov 244, Murodullayev 236, Angren&Oqqorgon 218, Abdullaxojaev 215, Sobitov 204, Sobirov 197, Djorayev 125. XULOSA webdevelopertk ga yuborildi: 8 ta avtomatik nazorat qoidasi mumkin (qisqa tashrif, rejadan tashqari, natijasiz, fotosuratsiz, GPS ochiq, signal yoqolgan, batareya past, radius buzilishi) - qoshimcha dastur/parol/OTP KERAK EMAS, hammasi mavjud MCP orqali.

*<- [[hub|Xarita]]*
