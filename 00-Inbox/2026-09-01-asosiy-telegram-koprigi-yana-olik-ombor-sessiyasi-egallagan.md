---
type: error
title: asosiy-telegram-koprigi-yana-olik-ombor-sessiyasi-egallagan
date: 2026-09-01
status: confirmed
verified: false
---

2026-09-01 TOPILDI (Ruslan hermes haqida sorayotganda tekshiruvda): asosiy Telegram kanali OLIK. DALIL: ikkala bun.exe (telegram MCP serveri) ham OMBOR sessiyasiga tegishli - jarayon zanjiri bun 20044 <- cmd 536 <- claude 18012 [OMBOR], bun 10952 ham osha zanjirda. Asosiy claude sessiyasida (PID 6220) birorta telegram serveri YOQ, channels/telegram/bot.pid fayli ham yoqolgan. Mening sessiyamda telegram MCP uzilgani tizim xabarida ham keldi. Yana: ombor sessiyasi bir marta yiqilgan (exit code -1073740791 = STATUS_STACK_BUFFER_OVERRUN), qorovul qayta kotargan. BU TAKRORLANUVCHI MUAMMO - vaultda 08-12, 08-14, 08-16, 08-21 sanalarida ayni shu nosozlik yozilgan. ILDIZ SABAB: Telegram ko'prigi TIRIK INTERAKTIV claude.exe sessiyasiga bogliq. Sessiya yiqilsa yoki band bolsa - aloqa uziladi. TOPILGAN YECHIM NOMZODI: hermes gateway install Windows'da SCHEDULED TASK sifatida ornatiladi (avtomatik logon'da) - ya'ni haqiqiy fon xizmati, interaktiv sessiyaga bogliq emas. DIQQAT: bir bot tokenida ikkita tinglovchi 409 Conflict beradi - otkazishda eskisini AVVAL ochirish shart.

*<- [[hub|Xarita]]*
