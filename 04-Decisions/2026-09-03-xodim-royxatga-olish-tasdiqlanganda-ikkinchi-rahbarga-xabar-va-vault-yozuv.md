---
type: decision
title: xodim-royxatga-olish-tasdiqlanganda-ikkinchi-rahbarga-xabar-va-vault-yozuv
date: 2026-09-03
status: confirmed
verified: false
---

2026-09-03 Ruslan sorovi: 'tasdiqlayman bosilganda sen ham xabar topasanmi'. Javob: yoq, men avtomatik bilmayman - tugmani mustaqil fon jarayoni (sd-listener.mjs) qayta ishlaydi. SHU SABAB QOSHILDI (sd-listener.mjs, regIshla funksiyasi): (1) qaror qilinganda (tasdiqlandi/rad etildi) BOSHQA rahbarga ham (bosmagan tomonga) alohida sendMessage yuboriladi - avval faqat bosgan odamning oz nusxasi tahrirlanardi, ikkinchisi bilmay qolardi; (2) natija Obsidian 06-Daily/<sana>.md ga yoziladi (royxatVaultYoz funksiyasi) - shu orqali men keyingi safar so'ralganda darhol bilaman. XATO TOPILDI VA TUZATILDI TEST PAYTIDA: dastlabki versiya new Date().toISOString() (UTC) bilan sana hisoblardi - Toshkent UTC+5 bolgani uchun kechqurun 19:00dan keyin (mahalliy) yozuv KECHAGI kun fayliga tushib qolardi. kecha()dagi kabi mahalliy getFullYear/getMonth/getDate ga ozgartirildi, tasdiqlandi (mahalliy 2026-09-03 vs UTC 2026-09-02 - farq amalda korsatildi). Vault yozish logikasi alohida test qilindi (fayl oxiriga togri qoshilishi tasdiqlandi, sinov qatori keyin tozalandi). Listener qayta ishga tushirildi, xatosiz. Tugma orqali HAQIQIY yakuniy sinov hali qilinmagan (jonli inson bosishi kerak).

*<- [[hub|Xarita]]*
