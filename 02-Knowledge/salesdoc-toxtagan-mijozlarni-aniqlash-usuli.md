---
type: knowledge
title: salesdoc-toxtagan-mijozlarni-aniqlash-usuli
date: 2026-08-18
status: confirmed
verified: false
---

2026-08-18: Ruslan 'Sobirov Botir xududida oldin xarid qilib keyin qoygan xaridorlar royxatini tashab ber' dedi. ISHLAGAN USUL (2 manba birlashtiriladi, chunki bitta tayyor hisobot yoq): (1) MIJOZLAR: POST /clients/client/JasonData2/?pageUrl=/clients/client/&active=Y -> 2261 mijoz; 'agent' maydonida agent ismi matn korinishida ('Sobirov Botirjon'), shu boyicha filtrlanadi -> 167 mijoz. (2) BUYURTMALAR: GET /orders/list/orders?date=FROM,TO -> {data:{orders:[[header],[row]...]}} ustunlar: client_id, agent_id, type, status, date, date_cancel, closed_amount. FAQAT type=='1' (buyurtma; type 3 = qaytarish) va date_cancel bosh bolganlar hisobga olinadi. CHEKLOV: 2 oylik oraliq ~3 MB, MCP uni faylga saqlaydi (JSON content-type bolgani uchun); 120 soniyadan oshsa fonga otadi. 6 oy uchun 3 ta sorov kerak boldi. ID BOGLASH: prefiks har sorovda boshqacha, pastki chiziqdan keyingi raqam boyicha birlashtiriladi. NATIJA (19.02-18.08.2026): Sobirovda 167 mijoz, 92 tasi shu davrda xarid qilgan, 28 tasi 45+ kundan beri buyurtma bermayapti, 75 tasi 6 oyda umuman buyurtma bermagan (ular uchun 6 oydan orqaga qarash kerak - qilinmadi). ENG MUHIM YOQOTISHLAR: QOYLIQ Sam MOYKA (12 buyurtma, 8.0 mln, 81 kun), Begzod Aka Ruchnoy Moyka (10 buyurtma, 4.4 mln, 99 kun), Sam Moyka Xasanboy (10 buyurtma, 3.9 mln, 78 kun), Avaz Robot Moyka Damariq (8 buyurtma, 3.8 mln, 48 kun). ISHLAMAGAN YOLLAR: /report/rfm/getData - fetch failed; /report/customer/clientListAjax agent[]=d0_95 filtri ISHLAYDI (166 yozuv) lekin javob HTML content-type bilan keladi va MCP KESIB tashlaydi, start/length paginatsiya ETIBORGA OLINMAYDI. AGENT ID: Sobirov Botirjon = d0_95 (ombor d0_10 'Sklad-VS Sobirov Botirjon'). Skript: scratchpad\proc.py (qayta ishlatish mumkin, boshqa agent uchun ism ozgartiriladi).

*<- [[hub|Xarita]]*
