---
type: fix
title: salesdoc-tolov-status-kodlari-aniqlandi
date: 2026-08-23
status: draft
verified: false
---

2026-08-23 ANIQLANDI: /payment/approval/getData javobidagi 'status' maydoni - 1 = TASDIQLANGAN, 0 = TASDIQLANMAGAN (kutmoqda). Dalil: 06-21 avgust oraligida 766 tolovdan 762 tasi status=1, 3 tasi status=0 va ular BIR NECHA KUN otsa ham status=0 bolib qolyapti (20.08 dagi Sobitov Abdurahmonning 3 ta tolovi 23.08 da ham tasdiqlanmagan) - demak status=0 vaqtinchalik emas, haqiqiy 'tasdiqlanmagan' backlog. 'approved_by' maydoni BU MAQSADGA YARAMAYDI - u barcha qatorlarda null (tasdiqlanganlarda ham). Yana bitta noaniq holat bor: 10.08 dagi 1,260,000 somlik tolov status=2 - bu nimani anglatishi HALI NOMALUM (bekor qilingan/rad etilgan bolishi mumkin), tekshirilmagan. Tasdiqlanmagan tolov summasini hisoblashda faqat status=0 olinadi.

*<- [[hub|Xarita]]*
