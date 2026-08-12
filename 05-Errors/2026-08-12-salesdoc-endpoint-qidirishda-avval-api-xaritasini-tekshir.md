---
type: fix
title: salesdoc-endpoint-qidirishda-avval-api-xaritasini-tekshir
date: 2026-08-12
status: draft
verified: false
---

SABOQ: 'сухой туман' prixodini topishda men /warehouse/list/receipt, /warehouse/list/arrival, /warehouse/list/prihod, /stock/list/receipt kabi bir nechta manzilni TAXMIN qilib sinadim - hammasi 404 berdi va vaqt ketdi. Aslida to'g'ri manzil (GET /warehouse/list/purchase?from=&to=&by=date) allaqachon 02-Knowledge/salesdoc-api-xaritasi.md faylida hujjatlashtirilgan edi (2026-08-10 dan). Ruslan menga skrinshot va keyin URL (/warehouse/view/listPurchase) yuborgach, shu faylda mos yozuvni topdim. QOIDA: SalesDoc'da har qanday yangi hisobot/sahifa manzilini qidirishdan OLDIN, avval 02-Knowledge/salesdoc-api-xaritasi.md faylini (Grep bilan kalit so'z bo'yicha) tekshirish kerak - ko'p sahifalar allaqachon xaritalangan, qayta taxmin qilib vaqt yo'qotmaslik kerak. Muvaffaqiyatli hisoblash usuli: /warehouse/list/purchase dan xom purchases+details ma'lumotini olib, /stock/stock/detail orqali mahsulot ID->nom bog'lanishini topib (nomida 'туман' so'zi bor ID'larni tanlab), keyin count'larni yig'ib, mahsulot nomidagi '1 Kg'/'0.5 L' belgisiga qarab kg'ga aylantirdim (natija: 2026-07-01 - 2026-08-12 oralig'ida ~373.5 kg).

*<- [[hub|Xarita]]*
