---
type: decision
title: masofadan-boshqarish-skilllar-ornatildi
date: 2026-08-17
status: confirmed
verified: false
---

2026-08-17: Ruslan 'kompyuter 99% yonimda bo'lmaydi, Telegram orqali vazifa beraman, sen kompyuterni boshqarishing kerak' dedi va 2 ta skill o'rnatishni buyurdi. O'RNATILDI (tekshirilgan): (1) anthropics/skills@mcp-builder - 102.4K o'rnatish, rasmiy Anthropic, C:\Users\user\.claude\skills\mcp-builder; eslatma - mavjud mcp-server-dev plagini bilan qisman dublikat. (2) ifuryst/open-codex-computer-use@open-computer-use - GitHub'da 1.7k yulduz, 160 fork, MIT; C:\Users\user\.claude\skills\open-computer-use (5 fayl). Windows/macOS/Linux uchun stdio MCP server: list_apps, click, type_text, press_key, scroll, drag, set_value. MUHIM: skill faqat YO'RIQNOMA - haqiqiy imkoniyat uchun 'npm i -g open-computer-use' kerak, HALI O'RNATILMAGAN (Get-Command bilan tekshirildi - yo'q). Avvalgi bahom NOTO'G'RI edi: men bu repo'ni 'ishonchsiz' deb aytgandim, aslida 1.7k yulduzli jiddiy loyiha - skills.sh dagi o'rnatishlar soni (864) repo sifatini to'liq aks ettirmas ekan. SABOQ: paket sifatini faqat o'rnatishlar soniga qarab baholamaslik, repo'ni ham ko'rish.

*<- [[hub|Xarita]]*

## 2026-08-17 - qo'shimcha
2026-08-17 (davomi): task-observer o'rnatildi - rebelytics/one-skill-to-rule-them-all@task-observer, 4.1K o'rnatish, GitHub 1.9k yulduz, CC BY 4.0, muallif Eoghan Henn; uch xil xavfsizlik auditidan o'tgan (Gen/Socket/Snyk - Low Risk). Joyi: C:\Users\user\.claude\skills\task-observer. Vazifasi: ish jarayonida ko'nikma yaxshilash imkoniyatlarini kuzatib borish. MUHIM ESLATMA skill hujjatidan: faqat description orqali ishga tushishi KAFOLATLANMAYDI - ishonchli ishlashi uchun CLAUDE.md ga yozuv yoki SessionStart hook kerak. 'computer-mcp' ALOHIDA QIDIRILDI: mustaqil bunday skill yo'q. Qidiruvda birinchi chiqqani allaqachon o'rnatilgan open-computer-use. Nomi aynan mos keladigan yagona narsa dmmulroy/.dotfiles@use-computer-mcp - 1 o'rnatish, shaxsiy dotfiles va SKILL.md fayli UMUMAN YO'Q (skills.sh sahifasida 'No SKILL.md available' deb yozilgan) - ya'ni bo'sh paket, o'rnatishdan foyda yo'q, o'rnatilmadi.
