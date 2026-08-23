---
type: knowledge
title: salesdoc-sms-tolov-xabarnomalari-tekshiruvi
date: 2026-08-23
status: confirmed
verified: false
---

2026-08-23 19:10 SMS TEKSHIRUVI (Ruslan soradi: 'kecha tolov qilgan barcha xaridorlarga sms yuborildimi?'). MANBALAR: GET /sms/message/list?from_date=&to_date= (SMS toplamlari, har birida template_title, sms_count, client_count, status, created_at) va GET /payment/approval/getData?from=&to= (tolovlar; javob {success, result:[[sxema],[qator]...]}, ustunlar: id, client_id, order_id, summa, date, agent_id, status, comment, type). NATIJA 22-AVGUST: tolov 53 yozuv, 44 turli mijoz, jami 14,877,500 som; status 1 (tasdiqlangan) 52 ta, status 0 (tasdiqlanmagan) 1 ta. SMS: 32 toplam; 46 mijozga YETIB BORGAN (status 'sent'); 6 mijozda 'waiting' holatida QOTIB QOLGAN - toplam 337 (5 mijoz, 10:10) va 343 (1 mijoz, 11:40). MUHIM: bu holat BUGUN (23-avgust) qayta sorovda ham 'waiting' - yani bir kundan keyin ham ozgarmagan, ozi ketmaydi. ARIFMETIK MOSLIK: 46 + 6 = 52 = tasdiqlangan tolovlar soni. Yani tizim HAR BIR tasdiqlangan tolov uchun SMS yaratgan, faqat 6 tasi jonatilmagan (bu item-by-item tekshirilmagan, faqat sonlar mos - Ruslanga shunday aytildi). BALANS MUAMMO EMAS: 21-avgust 17:48 da Ruslan 10,000 talik paket olgan, 9,996 qolgan. ANIQLANMAGAN ZIDDIYAT RUSLANGA AYTILDI: paket hisobida 'used: 4' turibdi, holbuki 22-avgustda 46 SMS ketgan - yo hisoblagich yangilanmagan, yo SMS eski paketdan yechilgan; bu SalesDoc tomonidagi hisob, taxmin qilinmadi. TAKLIF BERILDI: qotib qolgan SMS larni har kuni tekshirib, shunday holat bolsa Ruslanga xabar beradigan avtomatik nazorat qoyish (javob kutilmoqda).

*<- [[hub|Xarita]]*
