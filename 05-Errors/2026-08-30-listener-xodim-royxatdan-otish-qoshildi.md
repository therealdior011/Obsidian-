---
type: fix
title: listener-xodim-royxatdan-otish-qoshildi
date: 2026-08-30
status: draft
verified: false
---

2026-08-30: sd-listener.mjs faqat callback_query ni ishlardi, oddiy 'message' ni butunlay e'tiborsiz qoldirardi - shu sabab xodimlarni botga bog'lash IMKONSIZ edi. QO'SHILDI: sd-xodim.mjs (reestr) + listenerda xabarIshla/regIshla. OQIM: xodim @hoffen_auditbot ga ismini yozadi -> ARIZA (hech narsa yuborilmaydi) -> Ruslan yoki Bekzod tugma bosadi -> TASDIQLANGAN. XAVFSIZLIK QARORI: o'zini ro'yxatga qo'shish YETARLI EMAS, aks holda begona 'men Murodullayev Shoxrux' deb yozib ichki nazorat ogohlantirishlarini o'qib turardi. Fayl ataylab ikkiga bo'lingan: xodimlar[agent] tasdiqlangan, arizalar[chat_id] kutilmoqda - shuning uchun soxta ariza tasdiqlangan bog'lanishni bosib keta olmaydi. ISM MOSLASH: x<->h (Muxtorjon/Muhtorjon), dj<->j (Djo'rayev), apostrof turlari normalizatsiya qilinadi; agent_emas=true (hudud nomlari) va Demo chetlatiladi -> 8 ta haqiqiy xodim. 10 ta sinov o'tdi, eski ha|/yoq| oqimi buzilmadi. Listener qayta ko'tarildi PID 1276.

*<- [[hub|Xarita]]*
