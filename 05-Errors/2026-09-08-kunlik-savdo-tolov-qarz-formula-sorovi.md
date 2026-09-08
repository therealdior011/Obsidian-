---
type: fix
title: kunlik-savdo-tolov-qarz-formula-sorovi
date: 2026-09-08
status: draft
verified: false
---

2026-09-08 15:30-15:35 Ruslan aniq manbalarni korsatib tuzatdi: (1) Kassa /clients/finans/deliver?type=agent dan olinsin (avval notogri /dashboard/kassaIncome ishlatgandim); (2) Qarzdorlik 'Balansov Klentdan' (Balans boyicha qarz, mijoz balansi) olinsin, Savdo-Tolov ayirmasi EMAS. TEKSHIRILDI: /clients/finans/deliver sahifasi DataTables serverSide, haqiqiy manba /clients/finans/AjaxDeliver?agent_type=all&datestart=&endstart=&filter=&type=agent&confirm=0 (MUHIM: confirm=0 'Неподтвержденные' - bugungi hali tasdiqlanmagan kassa yozuvlari, confirm=1 bugun uchun 0 qaytardi, chunki tasdiqlash keyinroq boladi). Balans boyicha qarz allaqachon hisobot-tekshiruv.mjs da tekshir() ichida bor edi (Общий ustuni, /clients/transactions/JsonData) - qaytadan yozmadim. BUGUNGI (08.09) UCHTA VERIFIKATSIYALANGAN RAQAM: Savdo 22 767 500, Kassa 17 870 000, Balans boyicha qarz (jami, kunlik emas) 474 117 868. Ruslanga yuborildi, tasdiq soraldi ('togrimi?'). Tasdiqlangach SD-HisobotKunlik (22:00) avtomatikasiga qoshiladi. status: draft, verified: false.

*<- [[hub|Xarita]]*
