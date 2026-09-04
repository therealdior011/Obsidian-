---
type: fix
title: terminal-qorovuli-batareya-sozlamasi-tufayli-hech-qachon-ishlamagan
date: 2026-09-05
status: draft
verified: false
---

2026-09-05 02:56-02:59 TOPILDI VA TUZATILDI. MUAMMO: SD-TerminalQorovul vazifasi 05.09 00:23:38 da royxatga olingan (har 5 daqiqada qorovul.ps1 ni ishga tushirishi kerak edi), lekin Task Scheduler bo'yicha LastRunTime = 30.11.1999 ya'ni BIRONTA MARTA ishga tushmagan; LastTaskResult = 267011 (0x41303 SCHED_S_TASK_HAS_NOT_RUN). Ya'ni 4-sentabrdagi 'ombor boti 1 soat 38 daqiqa olik turgan' muammoning yechimi qogozda bor edi, amalda YOQ. ASL SABAB (dalil bilan): vazifada DisallowStartIfOnBatteries=True va StopIfGoingOnBatteries=True qolib ketgan, kompyuter esa batareyada ishlayapti - [System.Windows.Forms.SystemInformation]::PowerStatus.PowerLineStatus = Offline (Win32_Battery BatteryStatus=1). Windows batareyada bunday vazifani umuman boshlamaydi. TEKSHIRILDI: qolgan 9 ta faol SD- vazifada (AuditReport, HisobotDavriy, HisobotKunlik, KanalQorovul, MorningWatch, OmborZakaz, SorovEslatma, StoreWatch, Watchdog) bu sozlama False - muammo FAQAT shu bittasida edi, shuning uchun boshqa hisobotlar ishlayvergan. TUZATISH: Set-ScheduledTask orqali ikkala batareya cheklovi False ga otkazildi. SINOV (taxmin emas): (1) qolda ishga tushirildi 02:56:56 -> natija 0, bu vazifa tarixidagi BIRINCHI haqiqiy ishga tushish; uchala terminal (main 10040, ombor 14712, audit 10992) joyida qoldi, qorovul hech narsani ortiqcha ochirmadi, qorovul.log ga yangi qator yozilmadi (muammo yoq edi); (2) keyin jadval boyicha OZI ishga tushishi kutildi - 02:58:58 da avtomatik ishladi, natija 0, keyingisi 03:03:03. Endi 5 daqiqalik takrorlanish haqiqatan ishlayapti. SABOQ: Task Scheduler da vazifa 'Ready' korinishi va NextRunTime sanasi borligi u ISHLAYAPTI degani EMAS - LastRunTime ni alohida tekshirish kerak; noutbukda batareya sozlamasi jim turib butun himoyani ochirib qoyadi.

*<- [[hub|Xarita]]*
