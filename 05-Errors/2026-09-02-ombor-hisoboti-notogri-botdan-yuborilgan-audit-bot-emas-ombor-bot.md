---
type: fix
title: ombor-hisoboti-notogri-botdan-yuborilgan-audit-bot-emas-ombor-bot
date: 2026-09-02
status: draft
verified: false
---

2026-09-02 Ruslan (terminal) togri belgiladi: kechagi (2026-09-01) ombor hisoboti Bekzodga @hoffen_auditbot orqali yuborilgan edi, holbuki alohida ombor boti (OMBOR_BOT_TOKEN, username hoffen_ombor_managerbot, 2026-08-30dan beri .envda mavjud) aynan shu maqsad uchun edi - buni getMe orqali tekshirib tasdiqladim. SABAB: 09-01 kuni men Bekzodga TEST yuborganimda AUDIT_BOT_TOKENdan foydalandim (xato), keyinroq (soat 22:29, boshqa sessiya/jarayon tomonidan) ombor-rasm.mjs allaqachon OMBOR_GROUP_ID asosidagi togri logikaga yangilangan edi, lekin .envda OMBOR_GROUP_ID bor ekan va fallback filialidagi Bekzod qatori hali ham AUDIT_BOT_TOKENda qolgan edi - kechagi 19:00dagi avtomatik yuborish shu eski/notogri yoldan ketgan. TUZATILDI: fallback filialidagi Bekzod qatori OMBOR_BOT_TOKENga ozgartirildi, togri bot bilan qayta TEST yuborildi (Bekzod + Hoffen Ombor guruhi, ikkalasi ham muvaffaqiyatli). Bugungi 19:00dan boshlab togri bot ishlatiladi.

*<- [[hub|Xarita]]*
