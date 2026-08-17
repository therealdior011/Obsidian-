---
type: knowledge
title: SalesDoc-visit-getjson-tuzoqlari
date: 2026-08-17
status: confirmed
verified: false
---

sd-route.mjs yozilganda (2026-08-17) uchta tuzoq topildi va tekshirildi.

1) /report/visit/getjson TASHRIFLAR royxati EMAS - u REJA satrlarini ham qaytaradi. Tashrif qilinmagan satr ham mavjud boladi: visited=Neposeshennye, start/end=0000-00-00 00:00:00, summa=null. Satrlarni shunchaki sanash HAR DOIM ~100% bajarilish degan YOLGON natija beradi (hatto ertalab soat 5 da ham). Haqiqiy tashrif mezoni: visited=Poseshennye. 2957 satrda start-vaqt mezoni bilan atigi 1 tasida farq qildi. DIQQAT: mavjud sd-metrics.mjs shu endpointda satrlarni sanaydi - undagi jami_tashrif raqami shishgan bolishi mumkin.

2) Mijozning agent maydoni bir necha biriktirishni HTML br tegi bilan yopishtiradi: Yashnobod-Sergeli(Cht) + br + Offis(Vs). Bunda day maydoni FAQAT OXIRGI bolakning kunini beradi, yani day ga tayanish birinchi agentning rejasini butunlay yoqotadi (2260 mijozdan 288 tasi shunday). Togri usul: agent maydonini br boyicha bolib, har bolakning oxirgi qavsidan kunlarni olish. Nomning ozida ham qavs bolishi mumkin (Jalilov Ulugbek (Toshkent shaxri dilleri )(Pt,Sb)) - faqat OXIRGI qavs kesiladi.

3) day maydoni kop qiymatli: Pt,Sb - hatto haftaning barcha kunlari. Butun satrni solishtirish xato.

4) Mijozlar javobi orami {data:[...]} (topshiriqda {data:{data:[...]}} deyilgan edi) - ikkala shakl ham qollab-quvvatlansin.

TEKSHIRUV: 2026-08-15 uchun modul jami_tashrif=271 berdi, SalesDoc ozining Poseshennye soni ham aynan 271 - mos keldi.

*<- [[hub|Xarita]]*
