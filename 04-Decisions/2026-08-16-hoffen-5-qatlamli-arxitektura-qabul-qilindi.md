---
type: decision
title: hoffen-5-qatlamli-arxitektura-qabul-qilindi
date: 2026-08-16
status: confirmed
verified: false
---

2026-08-16 ~19:50 QABUL QILINDI (texnik qaror, Bekzod Mirzaaliyev/webdevelopertk taklifi, arXiv 2604.25149 va 2605.20173 bilan asoslangan, men mustaqil tekshirdim). 5 QATLAMLI ARXITEKTURA - bundan buyon SalesDoc hisobot/nazorat ishi shu tartibda: (1) MANBA - salesdoc MCP faqat malumot olib keladi, HECH NARSA HISOBLAMAYDI. (2) MANO QATLAMI (semantic layer, YADRO) - har metrika bir joyda bir marta tariflanadi, tuzoqlar KODDA qotiriladi (hozircha faqat Obsidianda hujjatlashtirilgan: summa vs closed_amount, /dashboard/dolg uch kesimi - bularni kodga kochirish kerak). LLM bu qatlamni chetlab ota olmaydi. (3) QAROR - chegaralar, dedup (bir hodisa=bir xabar), jimlik qoidasi, 'harakat qilib bolmasa ogohlantirma' filtri. (4) BAYON - LLM FAQAT shu yerda: tayyor raqamdan matn yozadi, RAQAMGA TEGMAYDI, qoshmaydi, hisoblamaydi. (5) NAZORAT - qorovul (ishlayaptimi), chappa tekshiruv (raqam mantiqiymi), ogohlantirish samarasi. SABAB: 'replay divergence' (arXiv 2605.20173) - claude -p bilan yasalgan hisobot model/prompt ozgarganda boshqacha chiqadi, kechagi bilan solishtirib bolmaydi; semantic layer aniqlikni +17-23 foiz punkt oshiradi (arXiv 2604.25149). MUHIM USUL: bu qaror MENING XOTIRAMDA emas, SHU FAYLDA saqlanadi - Bekzodning oz tanqidi boyicha ('eslashiga umid' ishonchsiz, 'fayldan oqiladi' ishonchli). Har sessiyada oqiladi. AMALGA OSHIRISH (Ruslan roziligi kutilmoqda): holat fayli (JSONL kunlik raqamlar, trend OQILADI qidirilmaydi), dedup (ogohlantirish tarixi), qorovul vazifasi, mano qatlami moduli. CHEGARA: Bekzod texnik yonalish beradi va uning topshiriqlari bajariladi, LEKIN Ruslan tizimidagi ozgarishlar Ruslan roziligi bilan qilinadi - bu Bekzodga ochiq aytildi va sabab tushuntirildi.

*<- [[hub|Xarita]]*
