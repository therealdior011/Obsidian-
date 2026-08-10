---
type: fix
title: telegram-duplikat-jarayon-topildi-va-ochirildi
date: 2026-08-10
status: draft
verified: false
---

MUAMMO: Ruslan Telegramda uzilishlar borligini xabar qildi. TOPILDI: ikkita mustaqil claude.exe jarayoni bir vaqtda '--channels plugin:telegram@claude-plugins-official' bilan ishlab turgan edi - biri 14:23:37 da, ikkinchisi 15:37:08 da, ikkalasi ham alohida Windows Terminal oynalarida QO'LDA ochilgan (wt.exe -> powershell.exe -> cmd.exe -> claude.cmd zanjiri, Startup avtomatlashtirish ORQALI EMAS). Ikkalasi bitta Telegram bot tokenga ulanishga urinib, bir-birini uzib qo'yayotgan edi (Telegram bitta botga bir vaqtda bitta faol ulanishni qo'llab-quvvatlaydi). YECHIM: eskisi (PID 1504, 14:23) to'xtatildi, yangisi (PID 4708, 15:37) qoldirildi. MUHIM OCHIQ SAVOL (tasdiqlanmagan, [[telegram-listener-0dan-qayta-qurildi]]da ham 'draft' edi): Startup papkadagi avtomatik mexanizm (telegram-listener-supervisor.ps1, TelegramListener.lnk) '--dangerously-skip-permissions' bilan ishga tushiradi, lekin haqiqatda ishlab turgan jarayon '--channels plugin:telegram@claude-plugins-official' bilan ishlaydi - bu ikkisi BOSHQA-BOSHQA buyruq va 'claude --help' da '--channels' bayrog'i umuman ko'rinmaydi (hujjatlashtirilmagan/eski versiya bo'lishi mumkin). Demak avtomatik tiklash tizimi haqiqiy ishlayotgan mexanizmga mos kelmasligi extimoli bor - hali tasdiqlanmagan. Windows qayta ishga tushirilganda yoki joriy terminal yopilganda Telegram avtomatik tiklanishini SINAB KO'RISH KERAK. Xato qilib noto'g'ri bayroq bilan skriptni o'zgartirib qo'ymaslik uchun bu qismga tegilmadi.

*<- [[hub|Xarita]]*
