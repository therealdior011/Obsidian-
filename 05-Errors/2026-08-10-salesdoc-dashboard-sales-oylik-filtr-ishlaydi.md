---
type: fix
title: salesdoc-dashboard-sales-oylik-filtr-ishlaydi
date: 2026-08-10
status: draft
verified: false
---

SalesDoc /dashboard/sales sahifasi datestart va endstart query parametrlarini qabul qiladi (masalan {"datestart":"2026-07-01","endstart":"2026-07-31"}) va o'sha oy uchun to'g'ri KPI/jadval (jumladan har agent uchun АКБ, ОКБ, Сумма) qaytaradi - standart holatda joriy oyni ko'rsatadi. Bu Ruslan 'Faxriddinning АКБ sini oyma-oy grafik qilib ber' deb so'raganda topildi va ishlatildi (yanvar-avgust 2026 uchun 8 ta so'rov bilan to'liq yillik trend chizildi: 64,65,80,90,89,84,81,49). Eslatma: avvalgi '05-Errors/2026-08-10-salesdoc-dashboard-sales-date-filter-ishlamaydi.md' yozuvida bu ishlamaydi deb yozilgan edi - ehtimol parametr nomi noto'g'ri sinalgan (masalan 'bydate' yoki boshqa kombinatsiya), to'g'ri parametr nomlari datestart/endstart ekan.

*<- [[hub|Xarita]]*
