---
type: fix
title: qarz-kunlik-hisobot-rasm-qilindi
date: 2026-09-09
status: draft
verified: false
---

Ruslan 08.09 kechqurun (23:08, Telegram) qarzdorlik kunlik hisoboti (savdo/tolov/qarzdorlik) matn korinishida kelayotganini payqadi - boshqa kunlik hisobotlar rasm bolib ketadi, bu bitta matn edi. Sabab: qarz-kunlik-yubor.mjs sendMessage (matn) ishlatgan, hisobot-kunlik-rasm.mjs kabi rasm-uslubidan foydalanmagan. Tuzatildi: yangi qarz-kunlik-rasm.mjs yaratildi (hisobot-uslub.mjs umumiy uslubidan foydalanadi, Edge orqali PNG qiladi, OWNER_CHAT_ID=104766999 ga sendPhoto bilan yuboradi). Task Scheduler SD-QarzKunlikYubor (har kuni 21:45) endi shu skriptga korsatadi, eski qarz-kunlik-yubor.mjs endi ishlatilmaydi (fayl qoldi, lekin chaqirilmaydi).

*<- [[hub|Xarita]]*
