---
type: decision
title: salesdoc-izoh-barcha-davrlarga-kengaytirildi
date: 2026-08-24
status: confirmed
verified: false
---

2026-08-24 05:35 IZOH BARCHA DAVRLARGA KENGAYTIRILDI (Bekzod yillik rasmni yuborib 'nega osgani yozilmagan, template edit qil' dedi). SABAB TOPILDI: 21-avgustda izohni FAQAT kunlik uchun ulagan edim (sd-growth-rasm.mjs da 'if (davr === kunlik)'), oylik va yillik eski bir qatorlik izoh bilan ketaverardi. TUZATISH: sd-izoh.mjs BUTUNLAY QAYTA YOZILDI - endi modul sifatida izohYoz(d, davr) funksiyasini eksport qiladi va sd-growth.mjs chiqishidan (d) foydalanadi, qoshimcha sorov QILMAYDI. sd-growth-rasm.mjs endi uni import qilib BARCHA davrlar uchun ishlatadi (kunlik/haftalik/oylik/yillik). ARIFMETIK USUL (kodda hujjatlashtirilgan): savdo = buyurtma x ortacha chek, shuning uchun savdo farqi ikkiga ajratiladi - buyurtma hissasi = (ord_hozir - ord_oldin) x chek_oldin; chek hissasi = (chek_hozir - chek_oldin) x ord_hozir; ikkalasining yigindisi savdo farqiga teng (yillikda tekshirildi: 869,098,580 + 804,586,280 = 1,673,684,860 vs haqiqiy farq 1,673,687,550 - yaxlitlash farqi). Chiqishda 'asosiy omil' ham korsatiladi. TEXNIK TUZOQ: 'if (import.meta.url === file://)' CLI tekshiruvi modul sifatida import qilinganda argv[1] undefined bolib YIQILADI - 'process.argv[1] &&' qoshildi. YOL-YOLAKAY TOPILMA (Bekzodga aytildi, hali tegilmagan): 22:00 dagi guruh xabari BOSHQA QUVURDAN chiqadi - scripts\salesdoc-evening-report.ps1 'claude -p' ni chaqirib MATNLI reyting yasaydi va telegram channel boti orqali yuboradi; sd-growth-rasm.mjs (rasmli osish) esa alohida. YANI IKKITA PARALLEL TIZIM ishlayapti. Ikkalasi ham ishlab turgani uchun hozircha tegilmadi, birlashtirish taklif qilindi.

*<- [[hub|Xarita]]*
