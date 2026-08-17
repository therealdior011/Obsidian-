---
type: decision
title: sd-listener-bridge-alohida-jarayon-qurildi
date: 2026-08-18
status: confirmed
verified: false
---

2026-08-18 Ruslan qaror berdi: HA/YOQ tugma listener ALOHIDA TERMINAL/JARAYON sifatida, asosiy Claude+Telegram sessiyasidan mustaqil ishlasin (2026-08-14 dagi saboq - bitta sessiyaga bogliq jarayon uzilib qolsa butun aloqa yiqiladi). AMALGA OSHIRILDI: (1) sd-listener-supervisor.ps1 - node sd-listener.mjs ni cheksiz tsiklda ishlatadi, yiqilsa 10s dan keyin qayta kotaradi. (2) Alohida PowerShell oynasida ISHGA TUSHIRILDI (Start-Process -WindowStyle Normal), PID 18464, log tasdiqladi: 'listener ishga tushdi, ruxsat: Ruslan aka, Bekzod Mirzaaliyev'. (3) LOGONDA AVTOMATIK: Task Scheduler AtLogOn trigger 'Access is denied' berdi (huddi TelegramListener uchun avval sinalmagan sabab bilan bir xil chegara) - shu sabab MAVJUD NAQSHGA otildi: Startup papkasi yorligi (C:\...\Startup\SD-ListenerBridge.lnk -> sd-listener-start.bat -> supervisor.ps1), xuddi AssistantRAG.vbs va TelegramListener.lnk kabi. (4) JAVOBSIZLIK QOIDASI QARORI: avtomatik shtraf YOQ - 30 daqiqadan keyin FAQAT Ruslanga shaxsiy ESLATMA boradi (sd-sorov-eslatma.mjs), shtraf hamon faqat tugma orqali ochiq tasdiq bilan beriladi. Sabab: jimlik signal, hukm emas - avvalgi tamoyilga mos. Task Scheduler 'SD-SorovEslatma' TOGRI ROYXATGA OLINDI (Daily trigger emas, Once+Repetition ishlatildi, bu tur AtLogOn kabi ruxsat muammosiga uchramadi) - har 15 daqiqada ishlaydi, keyingi: 18.08 04:17. Eskirgan sinov yozuvi (mswi1tvs0j, 17-avgustdagi guruh sinovi) 'sinov-eskirgan' deb belgilandi, eslatma tsiklidan chiqarildi. HOLAT: 1-bosqich (Audit agentlarga) TOLIQ ISHGA TUSHDI - qorovul, ertalabki kuzatuv, kunlik hisobot, marshrut moduli, HA/YOQ tugma + bridge + eslatma. Hali agentlarning ozига xabar YUBORILMAYDI (sinov davri, Ruslan talabi). Ochiq qolgan: GPS 9/11 buzuq, Djorayev/Sobirov bazaga kelmasligi qoidasi, sinov davri muddati.

*<- [[hub|Xarita]]*
