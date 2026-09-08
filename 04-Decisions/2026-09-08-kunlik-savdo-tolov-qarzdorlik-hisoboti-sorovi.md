---
type: decision
title: kunlik-savdo-tolov-qarzdorlik-hisoboti-sorovi
date: 2026-09-08
status: confirmed
verified: false
---

2026-09-08 Ruslan sorovi (audit-terminal orqali, ~13:04-14:03): har kuni 22:00gacha 'Kunlik savdo - Kunlik tolov = Kochadagi qarzdorlik' hisoboti kerak. TOPILDI: boshqa sessiya (ombor-terminal-7f, ehtimol) allaqachon sd-qarz-kunlik.mjs va SD-QarzKunlikSnapshot Task Scheduler vazifasini yaratgan (bugun 20:44), lekin faqat snapshot saqlaydi, Telegramga yubormaydi. Men bugungi hisobotni (savdo=22 767 500, tolov=17 870 000, osish=4 897 500, jami balans qarz=474 117 868) qolda hisoblab Ruslanga yubordim va ombor-terminal-7f ga xabar yozib muvofiqlashtirishni soradim - duplikat avtomatlashtirish qurmaslik uchun. Javob hali kelmadi.

*<- [[hub|Xarita]]*

## 2026-09-08 - qo'shimcha
2026-09-08 20:57 YAKUNLANDI: ombor-terminal-7f tasdiqladi - ular yuborish qismiga tegmaydi, faqat sd-qarz-kunlik.mjs (snapshot, 23:55 vazifasi) ularniki. Men qarz-kunlik-yubor.mjs yozdim (sd-qarz-kunlik.mjs dagi saqlaVaSolishtir() ni qayta ishlatadi, Telegramga AUDIT_BOT_TOKEN orqali yuboradi) va SD-QarzKunlikYubor Task Scheduler vazifasini qoshdim (har kuni 21:45, 22:00 muddatidan oldin). Ruslanga tasdiqlandi.
