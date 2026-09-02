---
type: fix
title: audit-bot-listener-tiqilib-qolgan-va-tuzatildi-tasdiqlash-tekshirildi
date: 2026-09-02
status: draft
verified: false
---

2026-09-02 ANIQLANDI: sd-listener.mjs (audit bot, /start royxatdan otish va shtraf-tasdiqlash tugmalarini eshituvchi long-poll jarayon, PID 1276, 2026-08-30dan beri uzluksiz ishlab turgan edi) getUpdates so'rovlarida soatlab (kamida 13:37dan 16:42gacha) 'fetch failed' xatosi berayotgan edi - uzoq umr korgan Node jarayonining tarmoq ulanish pooli tiqilib qolgani sabab (mening alohida node fetch chaqiruvlarim parallel ravishda muvaffaqiyatli ishlagani buni tasdiqladi - umumiy tarmoq muammosi emas edi). TUZATILDI: jarayon ozi Stop-Process bilan tugatildi, uni kuzatib turuvchi supervisor (sd-listener-supervisor.ps1, PID 2664, 2026-08-18dan beri ishlaydi) 15 soniyada yangi nusxani avtomatik kotardi, shundan keyin xato yozuvlari toxtadi. TASDIQLASH MEXANIZMI TOLIQ TEKSHIRILDI (Ruslan sorovi bilan): (1) arizaQoy - yozish ishlaydi, (2) haqiqiy tasdiqlash-sorovi xabari (inline tugmalar bilan) Bekzodga muvaffaqiyatli yetkazildi (sinov, keyin tozalandi), (3) arizaTasdiqla - arizalar->xodimlar kochishi togri ishlaydi. Faqat HAQIQIY tugma bosilishi (Telegramning ozidan callback_query) sinalmadi - buni faqat jonli inson bosishi orqali tekshirish mumkin, lekin listener hozir sog'lom va ulangan holda kutmoqda.

*<- [[hub|Xarita]]*
