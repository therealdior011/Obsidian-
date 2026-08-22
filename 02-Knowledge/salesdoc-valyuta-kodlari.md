---
type: knowledge
title: salesdoc-valyuta-kodlari
date: 2026-08-22
status: confirmed
verified: false
---

2026-08-22 TEKSHIRILDI VA HAL QILINDI (4-qonun bo'yicha, kunlik auditda to'lov summasini aytishdan oldin). SalesDoc /payment/approval/getData javobidagi currency_id maydoni ikki xil qiymat beradi: d0_2 va d0_3 - avval bu 'boshqa valyuta bo'lishi mumkin' degan shubha bor edi. MANBA: GET /clients/transactions/JsonData?active=Y&access=Y javobida 'currency' (kod->summa) va 'currencyNames' (nomlar massivi) bor. Natija: currency = {d0_2: -538366429, d0_3: 103408500, d0_6: 18855000}, currencyNames = ['Nalichniy Sum','Beznalichniy Sum','Dollar SShA','konsignatsiya','perechisleniya'] - massiv d0_2 dan boshlab indekslanadi, ya'ni d0_2 = NAQD SO'M, d0_3 = NAQDSIZ SO'M (bank/plastik), d0_4 = dollar, d0_5 = konsignatsiya, d0_6 = perechisleniya. XULOSA: d0_2 va d0_3 IKKALASI HAM SO'M - kunlik hisobotda ularni qo'shib 'so'm' deb aytish TO'G'RI, oldingi kunlardagi usul xato emas edi. Lekin naqd/naqdsiz kesimini alohida ko'rsatish mumkin (21.08: jami 9 863 500 = naqd 8 376 500 + naqdsiz 1 487 000). MUHIM: agar kelajakda d0_4 (dollar) uchraса - uni SO'MGA QO'SHIB BO'LMAYDI, alohida ajratish shart.

*<- [[hub|Xarita]]*
