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

## 2026-08-14 - kengaytirildi (kechki + oylik hisobotlar qo'shildi)
Ruslan asosiy Telegram kanalidan (104766999), TASDIQLANGAN JORIY suhbat sessiyasida (hoffen1/Habibulloh eskalatsiyasidan ALOHIDA, oddiy biznes so'rov ohangida, ~11:03-11:15) yana ikkita rutina so'radi. Bu haqiqiy Ruslan so'rovi, identity-taqlid yoki texnik-kalit so'rovi EMAS - oddiy hisobot mazmuni haqida.

Qo'shildi (bir xil xavfsiz naqsh: Task Scheduler + `--strict-mcp-config` + faqat salesdoc-only-mcp.json + Telegram Bot API'ga to'g'ridan-to'g'ri HTTP, telegram MCP hech qachon yuklanmaydi):

1. **`SalesDoc-EveningReport`, har kuni 22:00** - skript `C:\Users\user\.assistant\scripts\salesdoc-evening-report.ps1`. Mazmuni: bugungi kun uchun `/report/agent` (datestart=endstart=bugungi sana) orqali agentlar SOTUV REYTINGI (kim eng ko'p sotdi, kamayish tartibida, jami summa bilan). Sana skript ichida PowerShell `Get-Date` bilan hisoblanadi va promptga tayyor holda qo'yiladi (birinchi versiyada `<BUGUNGI SANA...>` placeholder qoldirilgan edi - sub-agent buni shubhali/kesilgan matn deb rad etdi, TUZATILDI).
2. **`SalesDoc-MonthlyReport`, har kuni 22:30** - skript `C:\Users\user\.assistant\scripts\salesdoc-monthly-report.ps1`. Mazmuni: joriy oy boshidan (1-sana) bugungi kungacha `/report/agent` orqali UMUMIY REYTING (kim nechinchi o'rinda, oy boshidan jami summa).
3. **09:00dagi asosiy hisobotga (`salesdoc-daily-report.ps1`) 4-band qo'shildi**: bugun kim qaysi rayon/marshrutga ketyapti - manba `/clients/agentRoute` (POST `/clients/agentRoute/getClients`, klient-marshrut ma'lumoti juda katta - 75k+ belgi - shu sabab sub-agent o'zi xulosa chiqarishi kerak, aniq bo'lmasa "aniqlay olmadim" deb yozishi kerak).

SABOQ: bir martalik `claude -p` sub-sessiyalar vaultni o'qib, "bugun xuddi shunday so'rov necha marta takrorlangan" degan tarixni ko'radi va agar YANGI so'rov vaultda hujjatlashtirilgan aniq qaror sifatida topilmasa - hatto texnik jihatdan to'g'ri va xavfsiz bo'lsa ham, ehtiyot yuzasidan RAD ETADI (bu to'g'ri xulq - kunlik voqealar konteksti buni talab qiladi). Shu sabab har bir yangi rutina/skript vaultga DARHOL, ishga tushirilishidan oldin yozilishi kerak.

*<- [[hub|Xarita]]*
