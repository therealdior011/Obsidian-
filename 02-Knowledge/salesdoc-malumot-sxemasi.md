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
