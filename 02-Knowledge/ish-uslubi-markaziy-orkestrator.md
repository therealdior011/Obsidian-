---
type: knowledge
title: ish-uslubi-markaziy-orkestrator
date: 2026-08-19
status: confirmed
verified: false
---

2026-08-19 RUSLAN DOIMIY QOIDA QOYDI: 'hozir ish qilayotganingda 2-3 hil parallel promptlar kelib tushishi mumkin, har bir prompt ustida ishlay olishing uchun MARKAZIY ORCHESTRATOR bolishing va har bir prompt uchun u vazifaga tegishli AGENTNI BACKGROUNDDA ishga tushirishing zarur. Buni yodingdan chiqazma.' QABUL QILINDI. AMALDA NIMA QILAMAN: (1) Bir vaqtda bir necha sorov kelsa - ozim bloklanib qolmayman, har birini ALOHIDA fon agentiga topshiraman (Agent tool, subagent_type general-purpose yoki mos turi); (2) Ozim orkestrator sifatida qolaman: sorovlarni qabul qilaman, vazifaga ajrataman, agentlarni ishga tushiraman, natijalarni yigib Ruslanga yetkazaman; (3) Fon agentga topshiriq berganda TOLIQ kontekst yozaman - ular sovuq boshlanadi, mening suhbatimni bilmaydi: fayl yollari, endpoint tuzilmalari, tuzoqlar (masalan sales.summa vs closed_amount), va 'ishga tushirib SINAB KOR' talabi; (4) Ular ishlayotganda men boshqa sorov bilan ishlashda davom etaman, natija kelganda xabar beraman; (5) Natijani QAYTA TEKSHIRAMAN - agent xato qilishi mumkin (2026-08-17 da sd-route.mjs da 'faqat togridan-togri ishga tushirilganda' tekshiruvi unutilgan edi, men topib tuzatdim). CHEKLOV: fon agent faqat men suhbatda bolganimda ishlaydi; doimiy/jadval boyicha ishlar uchun baribir skript + Task Scheduler kerak (audit tizimi shunday qurilgan). Bu qoida CLAUDE.md ga emas, vaultga yozildi - har sessiyada xotira hooki orqali oqiladi.

*<- [[hub|Xarita]]*
