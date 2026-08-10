---
type: fix
title: salesdoc-mcp-post-metodi-qoshildi
date: 2026-08-10
status: draft
verified: false
---

server.mjs'ga get_dashboard_page tool'iga method (GET/POST) va body parametrlari qo'shildi (fetchPage funksiyasi ham yangilandi), chunki 2026-08-10 navbar xaritalashda topilgan ko'p endpoint (masalan POST /staff/list/agent-paket - Agentlar ro'yxati) faqat POST qabul qiladi, eski kod faqat GET yuborardi. MUAMMO: kod yozilgan, lekin ishlayotgan MCP server jarayoni eski kod bilan davom etmoqda - o'zgarish kuchga kirishi uchun Claude Code sessiyasini/MCP ulanishini qayta ishga tushirish kerak. Qayta ishga tushgach POST /staff/list/agent-paket bilan sinab tasdiqlash kerak.

*<- [[hub|Xarita]]*
