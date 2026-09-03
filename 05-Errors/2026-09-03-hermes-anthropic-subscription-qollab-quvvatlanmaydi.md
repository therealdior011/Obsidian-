---
type: fix
title: hermes-anthropic-subscription-qollab-quvvatlanmaydi
date: 2026-09-03
status: draft
verified: false
---

2026-09-03: Hermes tekshirildi - jarayon tirik (PID 11116 hermes.exe + PID 20536 python), panel http://127.0.0.1:9119 HTTP 200. .env va config.yaml da HECH QANDAY LLM kalit yoq (ANTHROPIC/OPENAI/NOUS bosh) - 08-31dagi holat bilan bir xil, ozgarmagan. Ruslan Claude subscription (Pro/Max)ni kalit sifatida qoyishni sordi. TEKSHIRILDI: config.yaml provider royxatida (43-74 qator) Anthropic uchun FAQAT 'Direct Anthropic API (ANTHROPIC_API_KEY)' bor - subscription/OAuth yoli yoq (Codex va Nous uchun esa OAuth subscription bor, Anthropic uchun yoq). Ruslanga tushuntirildi: (1) alohida Anthropic API kalit sotib olish kerak (Claude.ai obunadan boshqa billing), yoki (2) obuna tokenini aylanma yol bilan ulash Anthropic foydalanish shartlariga zid va akkaunt bloklanish xavfi bor. Qaror kutilmoqda - hali hech narsa kiritilmadi.

*<- [[hub|Xarita]]*
