---
type: fix
title: salesdoc-browser-avtomatlashtirish-login-qilmagan
date: 2026-08-07
status: draft
verified: false
---

claude-in-chrome brauzer avtomatlashtirish tool'i (mcp__claude-in-chrome__*) hoffentash.salesdoc.io'ga kirmagan - alohida, autentifikatsiyalanmagan Chrome sessiyasi ekan (Ruslanning shaxsiy brauzeridan farqli). SalesDoc MCP server (mcp__salesdoc__get_dashboard_page) esa o'zining ichki sessiyasi bilan avtomatik login qiladi va aksariyat sahifalarni ochadi. Xulosa: 'Планы/Результаты' kabi Angular sahifalar uchun ma'lumotni faqat: (1) Ruslandan skrinshot/URL so'rash, yoki (2) uning DevTools'idan aniq AJAX endpoint manzilini (masalan Copy as cURL) olish orqaligina yechish mumkin - browser avtomatlashtirish orqali kirib bo'lmaydi (login talab qiladi, parolni o'zim kirita olmayman).

*<- [[hub|Xarita]]*
