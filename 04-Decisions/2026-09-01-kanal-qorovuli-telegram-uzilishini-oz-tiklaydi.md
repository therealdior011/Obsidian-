---
type: decision
title: kanal-qorovuli-telegram-uzilishini-oz-tiklaydi
date: 2026-09-01
status: confirmed
verified: false
---

2026-09-01 BEKZOD TALABI: 'mcp uzilmasligi kerak, ikkala botga ham alohida kanal qur'. HOLAT: kanallar ALLAQACHON alohida edi (tekshirilgan: asosiy PID 6220 -> bun 14080 -> channels/telegram -> token 6756502834 -> @hoffenotchot_bot; ombor PID 12780 -> bun 18512 -> channels/telegram-ombor -> token 8840208844 -> @hoffen_ombor_managerbot). Asl ehtiyoj - UZILMASLIK. QURILDI: scripts/kanal-qorovul.ps1 + SD-KanalQorovul vazifasi (har 10 daqiqa). TEKSHIRUV USULI: bot.pid faylidagi jarayon tirikmi (bot.pid ni telegram serverining O'ZI yozadi, ya'ni 'jarayon bormi' dan kuchliroq dalil) + getMe bilan token amal qiladimi. SINOV PAYTIDA MUHIM KAMCHILIK TOPILDI VA TUZATILDI: telegram serveri o'lsa-yu Claude sessiyasi TIRIK qolsa, qorovul hech narsa qilmasdi - u faqat sessiya o'lganda ishlaydi. Natijada sessiya ishlaydi, Telegram aloqasi yo'q, hech kim sezmaydi. Tuzatish: server o'lgan bo'lsa SESSIYA to'xtatiladi, qorovul uni yangi MCP serverlari bilan ko'taradi. JONLI SINOVDAN O'TDI: ombor serveri (PID 18512) ataylab o'ldirildi -> qorovul aniqladi -> sessiyani to'xtatdi -> 70 soniyada yangi server (PID 5804) bilan tiklandi. ASOSIY KANAL: uni tashqaridan ko'tarib bo'lmaydi (Claude sessiyasi ichida), shuning uchun o'lsa Ruslanga to'g'ridan-to'g'ri Bot API orqali ogohlantirish ketadi - bu MCP dan mustaqil va MCP o'lganda ham ishlaydi.

*<- [[hub|Xarita]]*
