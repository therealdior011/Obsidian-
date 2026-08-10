---
type: fix
title: salesdoc-hali-qabul-qilinmagan-kassa-endpoint-topildi
date: 2026-08-10
status: draft
verified: false
---

Ruslan 'hali qabul qilinmagan kassa qancha' deb so'raganda, avval taxminiy hisob (savdo-kassa farqi, ~20,218,000) berilgan edi - keyin Ruslan screenshot yubordi: to'g'ri manba /payment/approval sahifasi ('Подтверждение оплаты агентов', 'Неподтвержденные' filtri). API: GET /payment/approval/getData?from=YYYY-MM-DD&to=YYYY-MM-DD - qaytaradi result[] massiv, ustunlar orasida 'status' maydoni bor: status=0 -> hali tasdiqlanmagan (agentda turgan pul), status=1 -> tasdiqlangan/kassaga tushgan (bu SUM aynan /dashboard/kassaIncome jamiga teng chiqdi - screenshot bilan tasdiqlandi), status=2 -> bekor qilingan/o'chirilgan. 2026-08-10 kuni: status=0 jami 15,854,000 so'm (45 ta), status=1 jami 7,640,000 so'm (4 ta). Bu aniqroq - avvalgi taxminiy (savdo-kassa farqi) usulidan farqli, chunki savdo summasi va agentlar naqd yig'gan summa bir-biriga bevosita bog'liq emas (mijoz oldingi qarzini ham to'lashi mumkin).

*<- [[hub|Xarita]]*
