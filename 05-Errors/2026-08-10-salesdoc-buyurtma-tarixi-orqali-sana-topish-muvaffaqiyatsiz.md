---
type: fix
title: salesdoc-buyurtma-tarixi-orqali-sana-topish-muvaffaqiyatsiz
date: 2026-08-10
status: draft
verified: false
---

Doston ishga kirgan sanasini aniqlash uchun /orders/list/orders endpointidan uzoq davr (2024-2026) so'ralganda MCP ulanishi (salesdoc server) uzilib qoldi (Connection closed). Qisqaroq davr (2 oy, 2026-06-01..2026-08-10) 3.2 million belgi/191925 qator qaytardi - juda katta, deyarli har bir buyurtma to'liq mahsulot ro'yxati bilan qaytadi. Xulosa: bu endpoint orqali butun tarixni skanerlab 'birinchi buyurtma sanasi' topish amaliy emas (token/vaqt narxi juda katta, server crash qiladi). Kelajakda shunga o'xshash so'rov kerak bo'lsa - kichik oyma-oy bo'laklarga bo'lib, faqat kerakli agent nomini grep qilib chiqish kerak (butun javobni o'qimasdan), va eng qadimgi oydan boshlash (masalan orqaga qarab binary search).

*<- [[hub|Xarita]]*
