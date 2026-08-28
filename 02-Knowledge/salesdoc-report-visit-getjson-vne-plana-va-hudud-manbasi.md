---
type: knowledge
title: salesdoc-report-visit-getjson-vne-plana-va-hudud-manbasi
date: 2026-08-17
status: confirmed
verified: false
---

2026-08-17 KUNLIK HISOBOTNING 2 TA ESKI 'aniqlay olmadim' BANDI YOPILDI. /report/visit/getjson (GET, parametrsiz) - oxirgi ~8 kunlik BARCHA tashriflar (2957 yozuv, 1.09 MB - toolga sigmaydi, faylga tushadi, PowerShell bilan parse qilinadi). Javob: data[0] = SXEMA qatori (ustun nomlari/caption), data[1..] = ARRAY korinishidagi qatorlar, 16 ta ustun: 0 catclient, 1 summa, 2 agent, 3 clientId, 4 start, 5 end, 6 date, 7 visited (Posesenniye/Neposesenniye), 8 planed (Planoviye/VNEPLANOVIYE), 9 client, 10 order, 11 reject, 12 photo, 13 clientChannel, 14 city=TERRITORIYA (tuman nomi), 15 clientInn. BU NIMA BERADI: (a) 8-ustun = 'Vne plana' korsatkichi - kunlik hisobotning 1-bandi endi javobli; (b) 14-ustun = agent->rayon/marshrut biriktirilishi - 4-band uchun /clients/agentRoute (75000+ belgi, token limitidan oshardi) ONING ORNIGA SHU ISHLATILADI, ANCHA ARZON. TASDIQ: 17.08 uchun visit-report yozuv soni (315) /report/workingTime dagi 'Plan' ustunlari yigindisi (315) bilan AYNAN MOS TUSHDI - ikki mustaqil manba. TUZOQ: 'reja' deb visit-report qator sonini olish XATO - u plan+vneplan yigindisi; haqiqiy reja /report/workingTime 'Plan' ustunida (masalan Boxodirxoja 15.08: workingTime Plan=27, visit-report 42 qator, tashrif 41, shundan 15 tasi vneplan).

*<- [[hub|Xarita]]*

## 2026-08-28 - qo'shimcha
2026-08-28 QAMROV FOIZI TUZOGI: /report/visit/getjson reja satrlari ichida FAQAT dala agentlari emas - "Offis" va bo'sh marshrut slotlari (masalan "Yashnobod & Sergeli") ham reja satrlari oladi. 27.08: jami reja 349 satr, bajarilgan 255 -> 73% ko'rinadi; lekin Offis 53 va Yashnobod & Sergeli 36 satrni tashlab yuborsak, 9 ta dala agenti bo'yicha 255/260 = 98%. 26.08 da ham xuddi shunday: 250/293=85%, dala bo'yicha 250/258=97%. Ya'ni "qamrov tushdi" degan xulosa ofis reja satrlari sonining o'zgarishidan kelib chiqishi mumkin (26.08 da Offis 11 satr, 27.08 da 53 satr). QOIDA: qamrov foizini har doim dala agentlari kesimida hisoblash, Offis va tashrif qilmagan bo'sh marshrut slotlarini alohida qatorda ko'rsatish.
