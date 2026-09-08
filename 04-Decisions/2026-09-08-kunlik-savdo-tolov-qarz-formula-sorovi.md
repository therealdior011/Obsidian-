---
type: decision
title: kunlik-savdo-tolov-qarz-formula-sorovi
date: 2026-09-08
status: confirmed
verified: false
---

2026-09-08 15:01-15:05 Ruslan soradi: har kuni 22:00da 'Kunlik Savdo - Kunlik tolov = Kochadagi qarzdorlik' formulasi kerak. Darhol tekshirib korish soraldi ('hozir yubor bir koray'). BAJARILDI: hisobot-tekshiruv.mjs dagi tekshir() funksiyasidan foydalanib (borini ishlat qoidasi) bugungi (08.09) haqiqiy Savdo (22 757 500) va Kassa/tolov (32 393 000) SalesDoc'dan olindi, ayirma -9 635 500 chiqdi. MUHIM TOPILMA: bu manfiy son, sababi 'kassa' bugun tushgan PULNI korsatadi - unga OLDINGI kunlardagi qarz tolovlari ham kiradi, faqat bugungi savdo tolovlari emas. Shuning uchun oddiy ayirma haqiqiy 'kochadagi qarzdorlik' emas (bu tushuncha SalesDocda alohida umumiy balans korsatkichi, ~460-498 mln atrofida). Ruslanga bu farq ochiq tushuntirildi, ikki variant taklif qilindi: (a) shu formula ogohlantirish bilan davom etsin, (b) umumiy qarz balansi ham qoshilsin. Javob kutilmoqda - shundan keyin SD-HisobotKunlik 22:00 avtomatikasiga qoshiladi. Skript: sd-pipe/_kunlik-qarz-formula.mjs (bir martalik tekshiruv, hali doimiy modul emas). status: draft, verified: false.

*<- [[hub|Xarita]]*
