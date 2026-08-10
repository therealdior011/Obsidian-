---
type: fix
title: salesdoc-uzoq-davr-xodim-tarixi-tuzatildi
date: 2026-08-10
status: draft
verified: false
---

MUAMMO: /orders/list/orders orqali xodimning uzoq muddatli tarixini (masalan ishga kirgan sana) so'rash muvaffaqiyatsiz bo'lardi - bu endpoint har buyurtmani TO'LIQ mahsulot ro'yxati bilan qaytaradi, 2 oy uchun ham 3.2 million belgi/191925 qator bo'lgan, uzoqroq davr so'ralsa MCP ulanishi uziladi. YECHIM: C:\Users\user\.claude\mcp-servers\salesdoc\server.mjs ga yangi 'find_agent_orders' tool qo'shildi - bu server ICHIDA (Node.js) oy-oy skanerlaydi, mahsulot satrlarini (sales) tashlab yuboradi, faqat berilgan agent nomiga (created_by/updated_by) mos buyurtma qatorlarini filtrlaydi va FAQAT qisqa xulosa (buyurtmalar soni, jami closed_amount, birinchi/oxirgi sana) qaytaradi - hech qachon katta ma'lumot Claude kontekstiga o'tmaydi. TEKSHIRILDI: standalone Node skript bilan sinaldi (Sobitov Abdurahmon, 2026-05..2026-08, 4 oy, har oyi ~1-2 soniya, jami togri natija: 167 buyurtma, 35,605,000 summa). Default oraliq: 2023-01-01 dan bugungacha, MAX_MONTHS=96 (8 yil) xavfsizlik chegarasi bilan. ENDI QOLGAN QADAM: bu o'zgarish faylga yozilgan, lekin joriy ishlab turgan MCP ulanishlarga (jumladan Telegram listener'ning claude.exe jarayoni) darhol ta'sir qilmaydi - keyingi yangi sessiya/qayta ulanishda avtomatik faollashadi. Telegram jarayonini qaysi PID ekanini aniq bilmaganim uchun majburan o'ldirmadim (o'zi shu jarayon bo'lishi mumkinligi xavfi bor edi).

*<- [[hub|Xarita]]*
