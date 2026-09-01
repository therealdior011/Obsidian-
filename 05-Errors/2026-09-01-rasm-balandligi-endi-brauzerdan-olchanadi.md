---
type: fix
title: rasm-balandligi-endi-brauzerdan-olchanadi
date: 2026-09-01
status: draft
verified: false
---

2026-09-01 TAKRORLANUVCHI XATO YOPILDI. Rasm balandligi qo'lda taxmin qilinardi (qator soni x taxminiy balandlik) va mazmun o'zgarganda rasm PASTDAN KESILARDI. Uchradi: 30-avgust ombor hisoboti, 1-sentabr MVP rasmi (mazmun 1700 px, rasm 1600 px - jamoaviy reyting jadvali qo'shilgach). YECHIM: hisobot-kunlik-rasm.mjs da olcha() funksiyasi - sahifaga document.documentElement.scrollHeight ni title ga yozadigan script qo'shiladi, Edge --dump-dom bilan o'qiladi, keyin AYNAN o'sha balandlikda --screenshot olinadi. Natija: kunlik 2256 px, MVP 1704 px - ortiqcha bo'sh joy ham yo'q, kesilish ham. O'lchash yiqilsa taxmin bilan davom etadi (hisobot to'xtamaydi). Bu naqshni boshqa rasm skriptlariga ham ko'chirish kerak: ombor-rasm.mjs, ombor-reja-rasm.mjs, sd-growth-rasm.mjs.

*<- [[hub|Xarita]]*
