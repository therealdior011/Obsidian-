---
type: fix
title: asosiy-telegram-ombor-tokeniga-ulanish-ildiz-sababi-topildi
date: 2026-09-04
status: draft
verified: false
---

2026-09-04 21:56 ILDIZ SABAB TOPILDI VA TUZATILDI (2026-09-01 va bugungi ikkinchi marta takrorlangan xato: asosiy sessiya tasodifan OMBOR bot tokeniga ulanib qolishi). DALIL: Windows'da USER darajasida doimiy 'TELEGRAM_STATE_DIR=C:\Users\user\.claude\channels\telegram-ombor' o'zgaruvchisi qolib ketgan ekan (ehtimol 2026-08-31 ombor sessiyasini sozlashda [Environment]::SetEnvironmentVariable orqali qo'yilib, o'chirilmagan). Ombor va audit supervisorlari bun --strict-mcp-config JSON orqali o'z STATE_DIR'ini MAJBURIY qayta yozgani uchun ta'sirlanmagan, lekin telegram-listener-supervisor.ps1 (asosiy) hech qachon :TELEGRAM_STATE_DIR ni o'zi bermagan - shuning uchun u global/standart telegram plagin konfiguratsiyasi orqali ishga tushganda ushbu ADASHGAN doimiy o'zgaruvchini meros qilib olib, OMBOR papkasi/tokeniga ulanib qolgan. Buni namoyish etuvchi dalil: bun ajdodlar zanjiri orqali ombor tokenidagi server (7980) ning ASOSIY claude.exe (5584) ostida ekani tasdiqlandi. YECHIM: (1) doimiy USER darajasidagi TELEGRAM_STATE_DIR o'zgaruvchisi butunlay o'chirildi ([Environment]::SetEnvironmentVariable(...,'User') bilan ), (2) telegram-listener-supervisor.ps1 ga endi :TELEGRAM_STATE_DIR = channels\telegram aniq berildi (ombor/audit kabi), bu skriptning boshiga ham shu tozalash kodi yozildi (kelajakda yana paydo bo'lib qolsa avtomatik o'chirilsin). YON TA'SIR: xato tuzatish paytida ombor kanalining bot.pid fayli bo'shab qoldi (ombor va noto'g'ri asosiy nusxa bir xil papkani ishlatgani uchun, xatoni o'chirganda ombor ning HAQIQIY, hech qachon o'lmagan jarayoni ham 'ko'rinmas' bo'lib qoldi) - bot.pid qo'lda tiklandi, jarayonning o'zi (PID 12724) hech qachon uzilmagan edi. NATIJA: uchala bot (asosiy/ombor/audit) endi mustaqil, to'g'ri sessiyalarda tasdiqlangan (bun ajdodlar zanjiri orqali tekshirildi - hech qanday aralashish yo'q).

*<- [[hub|Xarita]]*
