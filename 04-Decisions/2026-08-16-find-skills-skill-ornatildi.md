---
type: decision
title: find-skills-skill-ornatildi
date: 2026-08-16
status: confirmed
verified: false
---

2026-08-16 ~20:20 Ruslan 'githubdan findskills skillni topib ornat' dedi. TEKSHIRILDI - shu nom bilan IKKI XIL narsa bor: (A) vercel-labs/skills 'find-skills' - Vercel kompaniyasi nashri, oddiy skill, tizim sozlamasiga tegmaydi; (B) findskills.org - 94,000 skill katalogi, LEKIN egasi/kompaniyasi ochiq korsatilmagan (faqat mail@findskills.org), 'npx findskills-mcp init' Claude Code configini OZI ozgartiradi va GitHub avtorizatsiyasi soraydi. Ruslanga farq korsatildi, U (A) NI TANLADI. ORNATILDI: npx -y skills add vercel-labs/skills --skill find-skills --agent claude-code -> C:\Users\user\.claude\skills\find-skills\SKILL.md (8KB, BITTA fayl, faqat matn korsatma - skript/kod YOQ, tekshirdim). Ornatuvchi xavfsizlik bahosini korsatdi: Gen=Safe, Socket=0 alerts, Snyk=Med Risk (Snyk bahosini eslatib qoyish kerak). JONLI SINALDI: 'npx skills find telegram bot report' ishladi, natija qaytardi (eng kop 55 install). SKILL NIMA QILADI: skills.sh katalogidan skill qidiradi, ornatishlar soni va manba obrusiga qarab baholaydi (1K+ install afzal, 100 dan kam - ehtiyot; vercel-labs/anthropics/microsoft ishonchli manba deb belgilangan). Foydali buyruqlar: 'npx skills find <sorov>', 'npx skills add <owner/repo@skill> -g -y', 'npx skills update', 'npx skills init <nom>' (oz skillini yaratish). MUHIM ESLATMA: ornatuvchining ozi ogohlantirdi - 'skills run with full agent permissions', yani har yangi skill ornatishdan oldin ichini OQIB CHIQISH kerak.

*<- [[hub|Xarita]]*
