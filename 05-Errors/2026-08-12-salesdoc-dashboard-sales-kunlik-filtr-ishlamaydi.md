---
type: fix
title: salesdoc-dashboard-sales-kunlik-filtr-ishlamaydi
date: 2026-08-12
status: draft
verified: false
---

SalesDoc /dashboard/sales sahifasi 'bydate', 'date', 'filter' query parametrlariga javob bermaydi - doim oy boshidan hozirgacha jamlangan summani ko'rsatadi (label: 'Продажа за месяц'), kunlik emas. Kunlik/aynan bir kunlik agent reytingi kerak bo'lsa - /orders/list/orders?date=YYYY-MM-DD,YYYY-MM-DD dan xom buyurtmalarni olib, har birining 'sales' massividagi summa qiymatlarini order_id bo'yicha yig'ib, keyin created_by (agent) bo'yicha guruhlash kerak - qo'lda hisoblash orqali. 2026-08-12 da Ruslan 'bugungi kunlik savdo reytingi' so'raganda shu usul bilan hisoblandi (jami 13,468,500 so'm, 44 buyurtma).

*<- [[hub|Xarita]]*
