---
type: decision
title: ombor-hisoboti-tortta-alohida-rasmga-bolindi
date: 2026-09-01
status: confirmed
verified: false
---

2026-09-01 BEKZOD TALABI: 'Shoshilinch / Keyingi Navbatda / Asosiy Omborda yo'q / Xarakatsiz - alohida rasm qilib yasash kerak, 4 ta rasm yuboriladi ombor bo'yicha'. SABAB: bitta rasmda balandlik 3650 px ga yetgan - telefonda pastki bo'limlar ko'rinmasdi. YARATILDI: ombor-bolimlar.mjs - har bo'lim o'z sarlavhasi, sanasi va o'z KPI plitalari bilan mustaqil sahifa. ombor-rasm.mjs CLI shunga ulandi, --yubor endi 4 ta rasm yuboradi (guruh + Ruslan + Bekzod). Balandliklar: 1953/1749/1581/1569 px. QO'SHIMCHA XATO TOPILDI VA TUZATILDI: olcha() funksiyasi katta o'lchov oynasi (2000 px) bilan ishlaganda scrollHeight = max(mazmun, OYNA) qoidasi tufayli OYNA balandligini qaytarardi - natijada to'rtala rasm ham 1896 px chiqib, pastida ~400 px bo'sh joy qolgan edi. Endi o'lchov oynasi ATAYIN kichik (300 px), shunda har doim mazmun balandligi qaytadi. Bu tuzatish hisobot-uslub.mjs da, ya'ni hamma hisobotga tegishli.

*<- [[hub|Xarita]]*
