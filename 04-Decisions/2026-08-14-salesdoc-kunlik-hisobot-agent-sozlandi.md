---
type: decision
title: salesdoc-kunlik-hisobot-agent-sozlandi
date: 2026-08-14
status: confirmed
verified: false
---

Ruslan har kuni ertalab 9:00da SalesDoc bo'yicha (1) umumiy hisobot (marshrut/radius buzilishi, tasdiqlanmagan to'lovlar) va (2) agentlar bo'yicha qisqa jadval kelishini so'radi ([[2026-08-14-shubhali-tizim-dostup-sorovi-ruslan-kanalidan-eskalatsiya|hoffen1 muzokarasi davomida]]). Bu ALOHIDA hoffen1-telegram-mcp akkauntisiz, mavjud infratuzilma bilan hal qilindi:

- Skript: `C:\Users\user\.assistant\scripts\salesdoc-daily-report.ps1`
- Windows Task Scheduler vazifasi: `SalesDoc-DailyReport`, har kuni 09:00 (lokal vaqt)
- Mexanizm: skript `claude -p` orqali BIR MARTALIK (one-shot) sessiya ishga tushiradi, `--strict-mcp-config` + `C:\Users\user\.assistant\scripts\salesdoc-only-mcp.json` bilan FAQAT salesdoc MCP'ga ulanadi (telegram MCP MUTLAQO yuklanmaydi - shu orqali asosiy Telegram listener sessiyasi bilan to'qnashish/uzilish xavfi oldini olindi, [[2026-08-14-hoffen1-telegram-mcp-ornatildi-lekin-sessiya-uzildi|avvalgi voqeadan farqli o'laroq]]). Natija matni `<<<REPORT>>>...<<<END>>>` teglari orasidan ajratib olinadi, so'ng Telegram Bot API'ga (`https://api.telegram.org/bot<token>/sendMessage`) to'g'ridan-to'g'ri HTTP so'rov bilan yuboriladi (token `C:\Users\user\.claude\channels\telegram\.env`dan o'qiladi, chatga yozilmaydi).
- Log: `C:\Users\user\.assistant\scripts\salesdoc-daily-report.log`
- SINALDI (2026-08-14, ~15:40): qo'lda ishga tushirildi, 898 belgili hisobot yuborildi, asosiy Telegram aloqa kanali UZILMADI (muvaffaqiyatli, avvalgi hoffen1 uzilishidan farqli).

MUHIM: hisobot mazmuni (raqamlar to'g'riligi) hali INSON TOMONIDAN TASDIQLANMAGAN - avtomatik agent CLAUDE.md'dagi halollik qoidasiga bo'ysunadi (noaniq bo'lsa "aniqlay olmadim" deydi), lekin bu birinchi run, natija sifatini Ruslan birinchi haqiqiy 9:00 hisobotida tekshirishi kerak.

*<- [[hub|Xarita]]*
