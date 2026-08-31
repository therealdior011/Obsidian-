---
type: fix
title: note-ps1-bosh-title-parametri-tushib-qoladi
date: 2026-08-31
status: draft
verified: false
---

Muammo: CLAUDE.md dagi ko'rsatma bo'yicha "powershell -File ...\note.ps1 daily <bosh-qoshtirnoq> <matn>" chaqirilganda xato: "missing mandatory parameters: BodyParts". Sabab: -File rejimida bo'sh qo'shtirnoq argument sifatida umuman uzatilmaydi, natijada matn Title ga tushadi, BodyParts bo'sh qoladi. YECHIM: daily yozuvni nomli parametrlar bilan chaqirish - PowerShell ichida: & C:\Users\user\.assistant\scripts\note.ps1 -Type daily -Title (bosh satr) -BodyParts (matn). Boshqa turlar (fix, decision, knowledge) da title bo'sh emas, shuning uchun eski usul ham ishlaydi. Tekshirildi 2026-08-31 18:12 - nomli parametrlar bilan 06-Daily/2026-08-31.md ga muvaffaqiyatli yozildi.

*<- [[hub|Xarita]]*
