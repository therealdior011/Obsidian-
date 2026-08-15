---
type: knowledge
title: salesdoc-malumot-sxemasi
date: 2026-08-07
status: confirmed
verified: false
---

SalesDoc /orders/list/orders javobida ikki xil summa bor: 'sales' massividagi 'summa' - buyurtma qiymati (so'ralgan), 'orders' massividagi 'closed_amount' - yopilgan/tasdiqlangan summa. 7-avgust kuni: 52 zayavka, summa jami 15 511 000 so'm, lekin closed_amount hammasida 0 (hali yopilmagan). Egasi dashboard/hisobotda 0 ko'rgan - demak u closed_amount yoki shunga o'xshash 'yopilgan' ko'rsatkichni ko'rgan bo'lishi mumkin. /dashboard/sales sahifasida kunlik emas, oylik KPI bor ('Продажа за месяц' va h.k.), kunlik alohida KPI yo'q edi.

*<- [[hub|Xarita]]*

## 2026-08-10 - qo'shimcha
Butun SalesDoc navbar/API xaritasi (130+ yo'l, bo'limlarga ajratilgan) — [[salesdoc-api-xaritasi]] fayliga chiqarildi. Shu yerda ikkita eski ochiq muammo hal qilindi: Agentlar ro'yxati (POST /staff/list/agent-paket) va Planning/kunlik reja (/planning/monthly2/data).

## 2026-08-07 - qo'shimcha
Sotuv agentlari: /report/agent hisobotida 11 ta qator bor (config_agents endpoint ham 11 ta - ikki mustaqil manba mos keldi). 9 tasi aniq shaxs ismi (Abdullaxo'jaev Boxodirxo'ja, Muhammadjonov Muhtorjon, Sobirov Botirjon, Athamov Faxriddin, Murodullayev Shoxrux, Sobitov Abdurahmon, Ahmadjonov Doston, Muhammad Ali, Djo'rayev Shuxratbek), qolgan 2 tasi shaxs emas - 'Yashnobod & Sergeli' (hudud/marshrut nomi) va 'Offis' (ofis guruhi). SalesDoc'da 'zavod' (ishlab chiqarish) tushunchasi UMUMAN YO'Q - bu tizim van-sale/FMCG distribution (sotuv/ombor/agentlar) uchun, xodim rollari: agent, supervisor, expeditor, stockman, auditor. Zavod xodimlari ma'lumoti boshqa joyda saqlanishi kerak (SalesDoc'da emas).

## 2026-08-15 - qo'shimcha
2026-08-15 qoshimcha: /dashboard/dolg (qarzdorlik) sahifasida BIR XIL agent uchun BIR NECHTA TURLI 'Obshiy' qarz raqami chiqadi - sahifada bir nechta tab/bolim bor ('По заказам', 'По маршрутам', 'По агентам', ekspeditor kesimi va h.k.), har biri boshqa-boshqa summa qaytaradi (masalan Athamov Faxriddin uchun bir vaqtda -98,844,500 / -83,223,000 / -85,586,000 uchta xil qiymat chiqdi, get_dashboard_page bularni ajratib bermaydi - hammasi 'title: null' jadval sifatida qaytadi). Bu SalesDoc'ning /orders/list/orders'dagi 'summa' vs 'closed_amount' muammosiga oxshash - manbada bitta korinishdagi maydon aslida bir nechta boshqa-boshqa hisoblash usulini anglatishi mumkin. SABOQ: qarzdorlik sorаlganda, bitta raqamni tanlab tekshirmasdan aytmaslik kerak - foydalanuvchidan aniq qaysi kesim (umumiy/joriy davr) kerakligini sorash kerak, xuddi 'sales' vs 'closed_amount' holatidagi kabi.
