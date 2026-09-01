---
type: knowledge
title: hermes-agent-nous-research
date: 2026-08-31
status: confirmed
verified: false
---

2026-08-31 Ruslan "hermes install qil va agents dashboardini ishga tushur" dedi. Kompyuterda va vaultda "hermes" degan hech narsa yoq edi - qidiruv otkazildi.
NIMA EKAN: Hermes Agent - Nous Research ning ochiq kodli (MIT) shaxsiy AI agenti. Rasmiy repo github.com/NousResearch/hermes-agent, rasmiy sayt hermes-agent.nousresearch.com. Imkoniyatlari bizning stekka juda yaqin: doimiy xotira, oz konikmalarini yozadi, cron rejalashtiruvchi, Telegram/Discord/Slack shlyuzi, MCP serverlar, subagentlar. Web-panel: 'hermes dashboard' -> http://127.0.0.1:9119 (Status, Analytics, Logs, Config, API Keys, Skills, Sessions, Chat, Cron, Webhooks, Channels, MCP, Pairing, Profiles, System).
ORNATISH YOLI: rasmiy PowerShell skripti (hermes-agent.nousresearch.com/install.ps1). Skript YUKLAB OLINDI VA OQILDI (242 KB, 4666 qator) - toza: tashqi manzillar faqat astral.sh/uv, nodejs.org, git-for-windows, python.org, github.com/NousResearch. Obfuskatsiya, Defender istisnosi, parol/kalit ogirlash yoq. -SkipComputerUse berildi (u trycua/cua drayverini uchinchi tomon repodan tortadi - kerak emas), -SkipSetup va -NonInteractive ham.
ADASHTIRMASLIK KERAK: (1) Hermes JavaScript dvigateli (Meta, React Native) - butunlay boshqa narsa. (2) Nous ning "Hermes 3/4" LLM modellari - shu vendor, lekin boshqa mahsulot. (3) npm 'hermes' paketi 2014 yildan beri tashlangan. (4) npm 'hermes-agent' va 'hermes-web-ui' - RASMIY EMAS, uchinchi tomon operatorlari; ornatmaslik kerak.
WINDOWS CHEKLOVI: dashboard ichidagi Chat yorlig'i POSIX pty talab qiladi, native Windows Python da ishlamaydi (WSL2 kerak) - qolgan hamma bolimlar ishlaydi.

*<- [[hub|Xarita]]*
