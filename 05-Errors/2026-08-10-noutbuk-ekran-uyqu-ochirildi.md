---
type: fix
title: noutbuk-ekran-uyqu-ochirildi
date: 2026-08-10
status: draft
verified: false
---

Ruslan so'rovi bilan noutbukning ekran o'chishi va uyqu (sleep) rejimi butunlay o'chirildi (powercfg /change monitor-timeout-ac/dc 0, standby-timeout-ac/dc 0, hibernate-timeout-ac/dc 0) - ham tarmoqdan, ham batareyadan quvvatlanganda. SABAB: fon jarayonlari (Telegram listener, GitHub avtomatik sync har 30 daqiqada) noutbuk uxlab qolganda to'xtab qolmasligi kerak. Oldingi holat: ekran 10 daqiqadan (tarmoq)/4 daqiqadan (batareya) keyin o'char edi, uyqu esa allaqachon 'hech qachon'ga sozlangan ekan. Qopqoq (lid) yopilganda nima bo'lishi sozlamasi bu qurilmada SUB_BUTTONS ostida ko'rinmadi (LIDACTION GUID query bo'sh qaytdi) - ehtimol bu qurilma lid-switch'ni Windows'ga alohida bildirmaydi yoki desktop rejimida ishlaydi, tekshirilmagan/aniqlanmagan holatda qoldi.

*<- [[hub|Xarita]]*
