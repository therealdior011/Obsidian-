---
type: fix
title: powershell-json-array-indexing-xatosi
date: 2026-08-10
status: draft
verified: false
---

MUAMMO: SalesDoc /orders/list/orders javobini (nested JSON arraylar) PowerShell'da ConvertFrom-Json qilib, keyin Where-Object { $_[$idxType] -eq '2' } bilan filtrlaganda NOTO'G'RI natija chiqdi (34 ta 'qaytarish' deb topildi, aslida bor-yo'g'i 1 ta edi - Group-Object bilan tekshirilganda aniqlandi). SABAB: noaniq, ehtimol $rows array PowerShell'da PSCustomObject sifatida talqin qilinganda ba'zi elementlar sonini noto'g'ri hisoblagan. YECHIM: nested JSON massivlarni tahlil qilishda Where-Object o'rniga Group-Object bilan avval taqsimotni tekshirish kerak (masalan $rows | Group-Object { $_[$idx] }) - natija umumiy qator soniga teng chiqishi kerak, aks holda xisob-kitobga ishonmaslik kerak.

*<- [[hub|Xarita]]*
