---
type: fix
title: telegram-salesdoc-dostup-tekshiruvi
date: 2026-08-10
status: draft
verified: false
---

Tekshirildi: SalesDoc MCP (.claude.json da) GLOBAL ravishda ulangan - barcha loyiha/sessiyalarda (jumladan Desktop loyihasida ham) mavjud, faqat bitta joyga bog'liq emas. server.mjs ichida login/parol .env dan avtomatik amalga oshadi, sessiya cookie muddati tugasa avtomatik qayta login qiladi (mcp__salesdoc__salesdoc_relogin bilan ham majburiy qilish mumkin). Telegram plugin ham shu Claude Code sessiyasi ichida bun orqali ishlaydi (alohida background xizmat/scheduled task yo'q - Task Scheduler'da claude/telegram bilan bog'liq vazifa topilmadi). XULOSA: konfiguratsiya darajasida telegram va oddiy chat bir xil MCP ro'ziga ega bo'lishi kerak - agar telegramdan so'ralganda salesdoc ishlamagan bo'lsa, sabab kirish huquqi yo'qligi emas, balki: (1) o'sha payt boshqa sessiya/oynada ishlagan bo'lishi, (2) tool chaqirishdan oldin ToolSearch orqali sxema yuklanmagan bo'lishi, yoki (3) vaqtinchalik tarmoq/login xatosi bo'lishi mumkin. Aniq sabab uchun keyingi safar xato matni/screenshot kerak.

*<- [[hub|Xarita]]*
