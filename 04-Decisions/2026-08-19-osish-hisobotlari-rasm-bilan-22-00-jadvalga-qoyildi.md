---
type: decision
title: osish-hisobotlari-rasm-bilan-22-00-jadvalga-qoyildi
date: 2026-08-19
status: confirmed
verified: false
---

2026-08-19 OSISH HISOBOTLARI RASM KORINISHIDA JADVALGA QOYILDI (Ruslan talabi: 'kunlik 22:00 da tashlansin', 'rasmda chartlar va kompyuter savodhonligi past odam ham korib 100% tushuna olishi'). YARATILDI: sd-growth-rasm.mjs - sd-growth.mjs bilan raqam hisoblaydi (nazorat qatlamidan otadi), sd-rasm.mjs bilan HTML yasaydi, Playwright CLI bilan PNG qiladi, guruhga sendPhoto orqali yuboradi. JONLI SINALDI - kunlik hisobot guruhga yuborildi (message_id 20). UCHTA TEXNIK TOSIQ YECHILDI: (1) heredoc apostroflarni buzdi -> Write bilan qayta yozildi; (2) execFileSync('npx') Windows'da ENOENT, ('npx.cmd') esa EINVAL beradi -> execSync (shell orqali) ishlatildi; (3) Playwright brauzeri ornatilmagan edi -> npx playwright install chromium (bir martalik). JADVAL: SD-GrowthKunlik har kuni 22:00; SD-GrowthHaftalik har DUSHANBA 22:05 (hafta yakunlangach); SD-GrowthOylik har kuni 22:10; SD-GrowthYillik har kuni 22:15. Hammasi batareyada ishlaydi, uyqudan uygotadi. YANA BIR NOSOZLIK TUZATILDI: SD-StoreWatch 'Once' trigger bilan royxatga olingan edi va takrorlash davri tugagach QAYTA BOSHLANMAGAN (NextRunTime bosh edi, 18.08 21:50 dan beri ishlamagan) -> Daily trigger + Repetition bilan qayta royxatga olindi, endi har kuni 07:00 dan 10 daqiqada, 15 soat davomida. SABOQ: Task Scheduler'da takrorlanuvchi vazifa uchun 'Once' trigger YETARLI EMAS - Daily trigger + Repetition kerak, aks holda bir marta tugagach toxtaydi.

*<- [[hub|Xarita]]*
