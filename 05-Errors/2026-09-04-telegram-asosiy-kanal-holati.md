---
type: fix
title: telegram-asosiy-kanal-holati
date: 2026-09-04
status: draft
verified: false
---

2026-09-04: Asosiy Telegram kanal (Ruslan asosiy boti) MCP jarayoni o'lik topildi (bot.pid=16940, jarayon yo'q). Uni ushlab turadigan Claude sessiyasi (PID 12576) tirik, lekin ichidagi telegram server subprocess yiqilgan - tashqaridan qayta ko'tarib bo'lmaydi, faqat o'sha sessiya oynasini qayta ishga tushirish yordam beradi. kanal-qorovul.ps1 buni 19:52 dan beri har 10 daqiqada aniqlab, audit boti orqali ogohlantirish yuborib turibdi (log: kanal-qorovul.log). Ombor kanali (@hoffen_ombor_managerbot, ombor-terminal loyihasi) shu payt sog'lom edi - tirik, token OK.

*<- [[hub|Xarita]]*

## 2026-09-04 - qo'shimcha
2026-09-04 21:10: TUZATILDI. Asosiy sessiya (eski PID 12576) qayta ishga tushirildi, telegram-listener-supervisor.ps1 uni avtomatik ko'tardi, yangi telegram server PID 15096, token OK. YAKUNIY YECHIM: kanal-qorovul.ps1 ni o'zgartirdim - endi ASOSIY kanal ham OMBOR kanali kabi avtomatik tiklanadi (avval faqat ombor uchun avtomatik edi, asosiy uchun faqat ogohlantirish yuborilardi). MUHIM TUZOQ TOPILDI VA TUZATILDI: birinchi urinishda -Tuzat ni yangi ko'tarilgan sessiya hali MCP/telegram ulanishini tugatmagan paytda ishga tushirib yubordim - bot.pid hali eski bo'lgani uchun skript uni 'olik' deb hisoblab yana o'chirib yubordi (qayta-qayta o'chirish xavfi). Yechim: skriptga 120 soniyalik 'yangi boshlangan sessiya' chegarasi qo'shdim - agar tegishli claude.exe jarayoni shu chegaradan yosh bo'lsa, muammo deb hisoblanmaydi, hech narsa o'chirilmaydi. SD-KanalQorovul vazifasi har 10 daqiqada -Tuzat bilan ishlaydi, endi ikkala kanal ham shu orqali o'zi tiriladi.
