---
type: fix
title: kunlik-savdo-tolov-qarz-formula-sorovi
date: 2026-09-08
status: draft
verified: false
---

2026-09-08 15:30-15:35 Ruslan aniq manbalarni korsatib tuzatdi: (1) Kassa /clients/finans/deliver?type=agent dan olinsin (avval notogri /dashboard/kassaIncome ishlatgandim); (2) Qarzdorlik 'Balansov Klentdan' (Balans boyicha qarz, mijoz balansi) olinsin, Savdo-Tolov ayirmasi EMAS. TEKSHIRILDI: /clients/finans/deliver sahifasi DataTables serverSide, haqiqiy manba /clients/finans/AjaxDeliver?agent_type=all&datestart=&endstart=&filter=&type=agent&confirm=0 (MUHIM: confirm=0 'Неподтвержденные' - bugungi hali tasdiqlanmagan kassa yozuvlari, confirm=1 bugun uchun 0 qaytardi, chunki tasdiqlash keyinroq boladi). Balans boyicha qarz allaqachon hisobot-tekshiruv.mjs da tekshir() ichida bor edi (Общий ustuni, /clients/transactions/JsonData) - qaytadan yozmadim. BUGUNGI (08.09) UCHTA VERIFIKATSIYALANGAN RAQAM: Savdo 22 767 500, Kassa 17 870 000, Balans boyicha qarz (jami, kunlik emas) 474 117 868. Ruslanga yuborildi, tasdiq soraldi ('togrimi?'). Tasdiqlangach SD-HisobotKunlik (22:00) avtomatikasiga qoshiladi. status: draft, verified: false.

*<- [[hub|Xarita]]*

## 2026-09-08 - qo'shimcha
2026-09-08 15:40-15:50 Ruslan soradi 'shunda qarzdorlik oshdimi'. HALOL JAVOB: oldingi kun balansini saqlab qoymaganim uchun aniq solishtira olmadim, faqat oqim boyicha taxmin berdim (Savdo-Tolov=+4 897 500). SHUNDAN KEYIN QURILDI: sd-pipe/sd-qarz-kunlik.mjs - har kuni Savdo/Tolov(kassa, AjaxDeliver confirm=0)/Qarz(Balans boyicha) ni sd-qarz-kunlik.jsonl ga saqlaydi, oldingi kun bilan avtomatik solishtiradi (qarzOsishi maydoni). BUGUNGI (08.09) BIRINCHI YOZUV SAQLANDI: savdo 22 767 500, tolov 17 870 000, qarz 474 117 868 (oldingi=null, birinchi kun). AVTOMATIKA: Task Scheduler 'SD-QarzKunlikSnapshot', har kuni 23:55 (mavjud SD-HisobotKunlik 22:00 dan keyin, kun yakuniga yaqin), tekshirildi - State: Ready. ERTAGA (09.09) DAN BOSHLAB aniq kecha-vs-bugun solishtiruv mumkin bo'ladi. Rasm formatiga qoshish (Ruslan sorovi) hali qilinmadi - avtomatik 22:00 hisobotiga aralashtirmaslik uchun, uning aniq tasdigini ('togrimi?') kutmoqdaman. status: draft, verified: false.
