---
type: fix
title: oylik-tolov-qamrovi-trend-hisoblandi
date: 2026-08-12
status: draft
verified: false
---

Ruslan 'yanvardan beri qarzdorlik konversiyasi oyma-oy' so'radi. Aniq tarixiy qarz balansi SalesDoc'da saqlanmagani sababli, proksi sifatida har oy uchun (kassaga tushgan/savdo) nisbati hisoblandi - buning uchun /dashboard/kassaIncome sahifasi ham datestart/endstart parametrlarini qabul qilishi TASDIQLANDI (xuddi /dashboard/sales kabi). Natija (yanvar-iyul 2026): 86.7%, 107.6%, 88.7%, 100.7%, 96.0%, 88.3%, 96.6% - o'rtacha ~95%, aniq pasayish trendi YO'Q, barqaror tebranish. Bu 'to'lov qamrovi' ko'rsatkichi, real qarzdorlik balansi emas (chunki bir oyning kassasi oldingi oy qarzlarini ham qoplashi mumkin - shuning uchun ba'zi oylar 100%dan oshgan). Foydali: /dashboard/kassaIncome ham /dashboard/sales kabi datestart/endstart bilan istalgan oy uchun ishlaydi.

*<- [[hub|Xarita]]*
