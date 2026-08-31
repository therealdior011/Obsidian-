---
type: error
title: hisobot-ajratish-belgilari-ishonchsiz
date: 2026-08-31
status: confirmed
verified: false
---

2026-08-31 IKKINCHI XATO (kodlash tuzatilgandan keyin chiqdi). salesdoc-daily-report.ps1 hisobotni claude chiqishidan '<<<REPORT>>>...<<<END>>>' belgilari orasidan regex bilan ajratadi. Bu safar sub-sessiya natijani boshqa formatda (kod bloki + izoh) qaytardi, belgilar mos kelmadi va skript zaxira xabar yubordi: 'Ertalabki kunlik hisobot bugun avtomatik tayyorlanmadi'. DALIL: salesdoc-daily-report.log da hisobotning TO'LIQ va sifatli matni turibdi, lekin salesdoc-daily-report-last.txt da atigi 121 bayt zaxira xabar. Ya'ni ish bajarilgan, natija yo'qolgan. Xulosa: bugun ertalab hisobot chiqdi-yu BUZUQ kodlashda, kechqurun toza chiqdi-yu YUBORILMADI - ikkita alohida nosozlik. TUZATILISHI KERAK: ajratish qat'iy belgilarga tayanmasin. QO'SHIMCHA: log fayli Add-Content bilan kodlashsiz yoziladi, u ham buzuq - uchinchi mayda nuqta.

*<- [[hub|Xarita]]*
