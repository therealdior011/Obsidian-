---
type: fix
title: stop-hook-tail-sekinligi-tuzatildi
date: 2026-09-02
status: draft
verified: false
---

2026-09-02 ANIQLANDI VA TUZATILDI: Stop hookdagi telegram-reply-reminder.ps1 skripti Get-Content -Tail 400 orqali sessiya transkriptini oqirdi - Windows PowerShell 5.1'da -Tail katta faylda JUDA SEKIN (butun faylni oxirigacha oqiydi). Olchov: 914KB transkriptda 8s, 42MB transkriptda 3+ daqiqa TUGAMADI. Har javobdan keyin ishlagani uchun bu 'Moseying... running stop hooks 1/2 5m33s' korinishidagi uzoq qotib qolishlarga va foydalanuvchi keyingi promptini kormay qolayotganga oxshash holatga sabab bolgan (Ruslan sorovi bilan tekshirildi). TUZATILDI: fayl oxiridan faqat songgi 2MB'ni FileStream.Seek bilan oqiydigan Get-TailLines funksiyasi yozildi (Get-Content -Tail o'rniga). Yangi olchov: 914KB - 0.13s, 42MB - 0.04s. Skript to'liq test qilindi (real payload bilan, exit 0, logika ozgarmadi). memory-reminder.ps1 (ikkinchi Stop hook) tekshirildi - u sekin emas edi (vault skanerlash 0.13s), tuzatishga hojat yoq.

*<- [[hub|Xarita]]*
