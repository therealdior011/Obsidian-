---
type: error
title: hisobot-matni-cp866-da-buzilgan
date: 2026-08-31
status: confirmed
verified: false
---

2026-08-31 BEKZOD XABAR BERDI: Ruslanga borgan kunlik audit hisoboti buzuq matn bilan kelgan ('тАФ' o'rniga '—', 'ЁЯФО' o'rniga emoji, kirill 'Вне плана' -> '╨Т╨╜╨╡'). SABAB (tekshirilgan, taxmin emas): bu kompyuterda [Console]::OutputEncoding = CP866. salesdoc-daily-report.ps1 da 'claude -p' chiqishi UTF-8 da keladi, PowerShell uni CP866 deb o'qiydi va buzadi. DALIL: skript yuborilgan matnni salesdoc-daily-report-last.txt ga -Encoding UTF8 bilan saqlaydi, va O'SHA FAYLNING ICHIDA ham matn allaqachon buzuq (U+FFFD) - demak buzilish YUBORISHDA emas, bola-jarayon chiqishini O'QISHDA. Men avval 'yuborishda buzilgan' deb taxmin qilgandim - noto'g'ri edi. TUZATILDI uchala skriptda (daily/evening/monthly): (1) claude chaqirilishidan OLDIN [Console]::OutputEncoding va  UTF8 ga o'rnatiladi - asosiy tuzatish; (2) yuborish ham mustahkamlandi - Invoke-RestMethod PS 5.1 da hashtable body ni ANSI da yuboradi, endi ConvertTo-Json + UTF8.GetBytes + ContentType application/json. QO'SHIMCHA KUZATUV: bugungi vazifalar 17:34-17:44 oralig'ida to'p bo'lib ishlagan - kompyuter uzoq o'chiq turib yoqilganda hammasi quvib yetgan, ya'ni hisobotlar o'z vaqtida chiqmagan.

*<- [[hub|Xarita]]*
