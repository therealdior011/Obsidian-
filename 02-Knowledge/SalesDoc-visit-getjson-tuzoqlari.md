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

## 2026-08-26 - qo'shimcha
5) TUZOQ (2026-08-26 topildi): start/end maydonlarida sana bilan vaqt orasida IKKI PROBEL bor - masalan '2026-08-25  11:49:26'. JS'da new Date(s.replace(' ','T')) FAQAT birinchi probelni almashtiradi, natijada satr yaroqsiz bo'lib NaN qaytadi va tashrif davomiyligi hisoblanmaydi (jimgina 0 chiqadi, xato ko'rinmaydi). TO'G'RI USUL: s.trim().replace(/\s+/,'T'). _n150.mjs bunga qarshi .replace(/\s+/,' ') ishlatgan, lekin yangi skript yozilganda takrorlanadigan tuzoq. TEKSHIRUV: to'g'rilangandan keyin 24.08 uchun qisqa tashrif (<1 daq) soni 122 chiqdi - 25.08 kungi hisobotda qo'lda hisoblangan raqam bilan aynan mos keldi.

## 2026-08-27 - qo'shimcha
2026-08-27: 5-tuzoq (ikki probel) _a26.mjs da HAM bor ekan - qisqa tashrif (<1 daq) hisobi jimgina 0 qaytargan (26.08 hisoboti tayyorlanayotganda topildi). Sabab: replace(' ','T') faqat birinchi probelni almashtiradi -> ISO satr yaroqsiz -> NaN -> shart hech qachon bajarilmaydi, xato ko'rinmaydi. _a27.mjs da tuzatildi: String(x).trim().replace(/\s+/,'T'). Tuzatilgandan keyin 26.08 uchun 143 chiqdi va _dur27.mjs (mustaqil skript) bilan AYNAN mos tushdi. XULOSA: har kuni _aNN.mjs sed bilan ko'chirilganda bu tuzatilgan _a27.mjs dan ko'chirilishi kerak, _a26.mjs dan EMAS. Yana: agar qisqa tashrif soni 0 chiqsa - bu real natija emas, tuzoq belgisi.
