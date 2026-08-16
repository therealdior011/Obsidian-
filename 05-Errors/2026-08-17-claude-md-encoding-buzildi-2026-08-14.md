---
type: fix
title: claude-md-encoding-buzildi-2026-08-14
date: 2026-08-17
status: draft
verified: false
---

2026-08-17: HAL QILINDI. Fayl UTF-16LE (BOM FF FE, 6624 bayt) holatida turgan ekan - 14-avgustdan beri shu ko'yi qolgan. Fon agenti orqali UTF-8 (BOM'siz, 3359 bayt) ga o'tkazildi. Zaxira: C:\Users\user\.claude\CLAUDE.md.utf16.bak. MUHIM ANIQLIK: matn MD5 oldin/keyin AYNAN BIR XIL (904963B55B32A9BBD835E980AAB1675C), 47 qator, U+FFFD 0 ta, 23 ta em dash va 1 ta o'q butun. Ya'ni faylda BUZILGAN BELGI YO'Q EDI - men avval 'tire va o'q buzilgan' deb noto'g'ri aytgandim, bu UTF-16 matnni bir baytli kodlash bilan o'qish natijasidagi ko'rinish edi (harflar orasidagi 00 baytlar). SABOQ: kodlash muammosini ko'rganda darhol 'belgi buzilgan' deb xulosa qilmaslik - avval baytlarni Format-Hex bilan ko'rish kerak. SABAB (14-avgustdagi yozuvdan): ehtimol fayl Notepad'da ochilib noto'g'ri formatda saqlangan; zararli o'zgarish topilmagan, mazmun barqaror.

*<- [[hub|Xarita]]*
