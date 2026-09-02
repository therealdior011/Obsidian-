---
type: fix
title: sana-utc-mahalliy-xatosi-boshqa-skriptlarda-ham-tekshirildi
date: 2026-09-03
status: draft
verified: false
---

2026-09-03 Ruslan sorovi bilan barcha sd-pipe skriptlari (.mjs, hisobot va nazorat) toISOString().slice(0,10) uslubidagi UTC-sana xatosiga tekshirildi. TOPILDI: sd-run.mjs dagi bugun() funksiyasi xuddi shu xatoga ega edi - sd-state.jsonl (kunlik surat/trend) va sd-alerts.json (dedup) sanalarini UTC bilan hisoblardi, Toshkent mahalliy 00:00-05:00 oralig'ida buzuq (kechagi) sanani berardi. TUZATILDI: getFullYear/getMonth/getDate (mahalliy) ga otkazildi, --dry rejimda ishga tushirib tekshirildi, natija togri (2026-09-03). TA'SIR DARAJASI PAST edi amalda: SD-AuditReport vazifasi faqat 12:30 va 20:00da ishlaydi, bug oynasidan (00:00-05:00) tashqarida - hali xato yuz bermagan, lekin kelajakda jadval ozgarsa yoki qolda ishga tushirilsa xavfli edi. Boshqa hamma joyda (sd-audit-report.mjs KUN, ombor-rasm.mjs kecha()) allaqachon TOGRI mahalliy usul ishlatilgan ekan - faqat sd-listener.mjs (2026-09-02 tuzatilgan) va sd-run.mjs (bu safar) xato edi. Butun .assistant papkasi toliq skanerlandi (.mjs va .ps1), boshqa hech qanday UTC-sana yoki UtcNow patterni topilmadi.

*<- [[hub|Xarita]]*
