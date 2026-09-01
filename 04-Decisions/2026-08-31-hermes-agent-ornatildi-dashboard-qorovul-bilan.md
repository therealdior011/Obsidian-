---
type: decision
title: hermes-agent-ornatildi-dashboard-qorovul-bilan
date: 2026-08-31
status: confirmed
verified: false
---

2026-08-31 23:35-23:48 ORNATILDI VA TEKSHIRILDI. Hermes Agent v0.20.6 (2026.8.27), Nous Research. Joyi: C:\Users\user\AppData\Local\hermes (kod hermes-agent\, config.yaml, .env, skills\ - 58 ta konikma, sessions\, cron\, logs\). Buyruq: %LOCALAPPDATA%\hermes\bin\hermes.exe.
ORNATISH: rasmiy install.ps1 yuklab olindi va OQILDI (242 KB, 4666 qator - toza, obfuskatsiya/Defender istisnosi/kalit ogirlash yoq), keyin -SkipSetup -SkipComputerUse -NonInteractive bilan ishlatildi. Yonida keldi: uv 0.12.7, Python 3.11.16 (alohida, mavjud 3.12 ga tegilmadi), ffmpeg (Chocolatey orqali). Git 2.55 va Node 24.19 allaqachon bor edi.
PANEL: http://127.0.0.1:9119 - TIRIK, HTTP 200 tasdiqlangan. Faqat loopback (tashqi tarmoqqa ochilmagan).
QOROVUL: scripts\hermes-dashboard-supervisor.ps1 + Startup\HermesDashboard.vbs (yashirin). Har 30 soniyada HAQIQIY HTTP sorov yuboradi (jarayon tirik turib ichida qotib qolishi mumkin - shuning uchun "process bormi" tekshiruvi yetarli emas). Ketma-ket 3 marta javobsizlikdan keyin 'hermes dashboard --stop' bilan tozalab qayta kotaradi. Jarayon tutqichi saqlanmaydi - holat PORT orqali olchanadi, shuning uchun panelni kim kotarganidan qat'i nazar ishlaydi va sog'lom panelga TEGMAYDI (duplikat ochmaydi - tekshirildi).
--skip-build: har ishga tushishda Vite web interfeysini qaytadan yigadi (bir necha daqiqa), shuning uchun qayta kotarishda --skip-build ishlatiladi. Ketma-ket 2 muvaffaqiyatsiz urinishdan keyin ozi TOLIQ yigishga otadi ('hermes update' dan keyin dist eskirishi mumkin).
SINOV OTKAZILDI (taxmin emas): panel jarayoni qolda oldirildi -> qorovul 34 soniyada sezdi, 3 tasdiqdan keyin qayta kotardi, jami 85 SONIYADA tiklandi, HTTP 200 qaytdi.
OCHIQ MASALA: hech qanday LLM kaliti qoyilmagan (.env da ANTHROPIC/OPENAI/NOUS/OPENROUTER - hammasi bosh). Panel ishlaydi, lekin agentning ozi kalitsiz oylay olmaydi. Kalit panelning "API Keys" bolimidan yoki 'hermes setup' orqali kiritiladi.
WINDOWS CHEKLOVI: panel ichidagi Chat yorligi POSIX pty talab qiladi, native Windows Python da ishlamaydi (WSL2 kerak). Qolgan bolimlar ishlaydi.

*<- [[hub|Xarita]]*
