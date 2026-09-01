---
type: error
title: haftalik-trigger-quvib-yetmadi-ombor-hisoboti-hech-qachon-ketmagan
date: 2026-09-01
status: confirmed
verified: false
---

2026-09-01 TOPILDI (Bekzod 'ombor kontekstidan nima borayotganini tekshir' degani sababli): SD-OmborZakaz vazifasi 30-avgustda 'har dushanba 09:00' trigger bilan qo'yilgan edi, lekin BIR MARTA HAM ISHLAMAGAN. DALIL: LastRunTime = 11/30/1999 (hech qachon), LastTaskResult = 267011 (0x41303 = 'task has not yet run'), NextRunTime 07.09.2026 ga o'tib ketgan. SABAB: 31-avgust dushanba 09:00 da kompyuter o'chiq bo'lgan. StartWhenAvailable=True qo'yilgan bo'lsa ham Windows haftalik triggerni QUVIB YETMADI (o'sha kuni 17:34 da boshqa vazifalar quvib yetgan, bu esa yo'q). Ya'ni haftalik ombor hisoboti Ruslanga hech qachon avtomatik bormagan. TUZATILDI: vazifa HAR KUNI 09:00 ga o'tkazildi, kun tekshiruvi KODGA ko'chirildi (ombor-rasm.mjs --haftalik bayrog'i, dushanba bo'lmasa jim chiqadi). Sinovdan o'tdi: bugun seshanba -> 'bugun dushanba emas, yuborilmadi'. SABOQ: Windows'da kam uchraydigan (haftalik/oylik) triggerlarga ISHONMASLIK - kompyuter o'sha soatda o'chiq bo'lsa quvib yetmasligi mumkin. To'g'ri naqsh: kunlik trigger + kalendar tekshiruvi kodda (hisobot-davriy.mjs da ham shunday qilingan).

*<- [[hub|Xarita]]*
