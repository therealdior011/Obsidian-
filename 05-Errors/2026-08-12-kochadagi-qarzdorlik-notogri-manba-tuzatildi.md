---
type: fix
title: kochadagi-qarzdorlik-notogri-manba-tuzatildi
date: 2026-08-12
status: draft
verified: false
---

XATO: Ruslan 'ko'chadagi umumiy qarzdorlik' so'raganda, /dashboard/dolg sahifasidan foydalanib 716,546,780 so'm deb aytdim. Ruslan skrinshot yubordi (Sales Doctor - Transactions, 'Балансы клиентов' sahifasi): to'g'ri raqam -436,590,230 so'm ekan. SABAB: /dashboard/dolg sahifasida bir nechta o'xshash ko'rinishdagi jadval bor edi (turli qamrov: faol agentlar, ekspeditorlar, va yana bir jadvalda 'Ruslan Knyazov -547mln', 'Dostafka', raqamli kodlar kabi aniq mijoz bo'lmagan yozuvlar) - bularning qaysi biri 'to'g'ri' umumiy mijoz qarzi ekanini tekshirmasdan, birinchi jadvalni yig'ib noto'g'ri javob berdim. TO'G'RI MANBA: /clients/transactions ('Балансы клиентов' / Client Balances) sahifasi - bu maxsus mijoz balansi uchun mo'ljallangan, JSON endpoint /clients/transactions/JsonData?active=Y&access=Y. SABOQ (CLAUDE.md 4-qonun bilan mos): SalesDoc'da 'qarzdorlik'/'balans' kabi moliyaviy ko'rsatkichlar uchun BIR NECHTA sahifa bor va ular boshqa-boshqa qamrov/tarkibga ega - har doim eng maxsus/aniq nomli sahifani ('Балансы клиентов' aynan shu maqsad uchun) ishlatish kerak, umumiyroq ko'rinadigan sahifalarni ('Долги' - bu aralash/noaniq) emas. Kelajakda moliyaviy raqam so'ralsa, avval mos sahifa nomini navbar'dan aniq tanlash kerak.

*<- [[hub|Xarita]]*
