---
type: knowledge
title: tizim-inventarizatsiyasi-agentlar-avtomatik-jarayonlar
date: 2026-08-16
status: confirmed
verified: false
---

2026-08-16 ~20:35 TOLIQ TEKSHIRILDI (Ruslan sorovi: 'qanday agentlar bor, tahmin qilmay ayt va qayerda turadi'). (1) AI-AGENTLAR: BIZNING OZIMIZNIKI BITTA HAM YOQ - C:\Users\user\.claude\agents\ papkasi UMUMAN MAVJUD EMAS, loyiha darajasida ham yoq. Faqat tayyor kelganlar: Explore, Plan, general-purpose, claude-code-guide, statusline-setup (tizim ichida); agent-sdk-verifier-py/ts (plugins\cache\claude-plugins-official\agent-sdk-dev\unknown\agents\); analyzer/comparator/grader (skill-creator plagini ichida). (2) HAQIQIY ISHLAYOTGAN AVTOMATIK JARAYONLAR: Task Scheduler - SalesDoc-DailyReport (09:00), SalesDoc-EveningReport (22:00), SalesDoc-MonthlyReport (22:30), SD-Watchdog (10:00 va 23:00, bugun qurildi); Startup papkasi - AssistantRAG.vbs (RAG server, ISHLAYAPTI, health javob berdi: ok=true, 342 chunk, 2 python jarayoni 07.08 dan beri), TelegramListener.lnk. (3) MUHIM TUZATISH - MEN AVVAL NOTOGRI AYTGANMAN: bugun Ruslanga 'alohida fon-vazifa yoq' degandim - bu YARIM TOGRI edi. Task Scheduler'da rostdan yoq (ClaudeCode-TelegramListener ochirilgan), LEKIN Startup papkasida TelegramListener.lnk BOR - u C:\Users\user\.assistant\scripts\telegram-listener-start.bat ni ishga tushiradi. AMMO u HECH QACHON ISHLAMAGAN: yorliq 10-avgustda yaratilgan, kompyuter esa 05.08.2026 11:56 dan beri qayta yoqilmagan (LastBootUpTime tekshirildi) - logon bolmagani uchun trigger tushmagan. Yani Telegram aloqasi HOZIR HAM ochiq CLI oynasiga (PID 7316) bogliq. Kompyuter qayta yoqilganda bu yorliq birinchi marta sinaladi. SABOQ: 'fon-vazifa yoqmi' degan savolga faqat Task Scheduler'ni tekshirib javob berish YETARLI EMAS - Startup papkasi, registry Run kalitlari ham avtomatik ishga tushirish yollari.

*<- [[hub|Xarita]]*
