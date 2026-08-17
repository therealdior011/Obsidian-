---
type: knowledge
title: salesdoc-report-visit-getjson-vne-plana-va-hudud-manbasi
date: 2026-08-17
status: confirmed
verified: false
---

2026-08-17 KUNLIK HISOBOTNING 2 TA ESKI 'aniqlay olmadim' BANDI YOPILDI. /report/visit/getjson (GET, parametrsiz) - oxirgi ~8 kunlik BARCHA tashriflar (2957 yozuv, 1.09 MB - toolga sigmaydi, faylga tushadi, PowerShell bilan parse qilinadi). Javob: data[0] = SXEMA qatori (ustun nomlari/caption), data[1..] = ARRAY korinishidagi qatorlar, 16 ta ustun: 0 catclient, 1 summa, 2 agent, 3 clientId, 4 start, 5 end, 6 date, 7 visited (Posesenniye/Neposesenniye), 8 planed (Planoviye/VNEPLANOVIYE), 9 client, 10 order, 11 reject, 12 photo, 13 clientChannel, 14 city=TERRITORIYA (tuman nomi), 15 clientInn. BU NIMA BERADI: (a) 8-ustun = 'Vne plana' korsatkichi - kunlik hisobotning 1-bandi endi javobli; (b) 14-ustun = agent->rayon/marshrut biriktirilishi - 4-band uchun /clients/agentRoute (75000+ belgi, token limitidan oshardi) ONING ORNIGA SHU ISHLATILADI, ANCHA ARZON. TASDIQ: 17.08 uchun visit-report yozuv soni (315) /report/workingTime dagi 'Plan' ustunlari yigindisi (315) bilan AYNAN MOS TUSHDI - ikki mustaqil manba. TUZOQ: 'reja' deb visit-report qator sonini olish XATO - u plan+vneplan yigindisi; haqiqiy reja /report/workingTime 'Plan' ustunida (masalan Boxodirxoja 15.08: workingTime Plan=27, visit-report 42 qator, tashrif 41, shundan 15 tasi vneplan).

*<- [[hub|Xarita]]*
