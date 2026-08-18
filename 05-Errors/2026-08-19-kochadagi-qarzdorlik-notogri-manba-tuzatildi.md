---
type: fix
title: kochadagi-qarzdorlik-notogri-manba-tuzatildi
date: 2026-08-19
status: draft
verified: false
---

2026-08-19 QARZDORLIK ENDPOINTI TOLIQ OCHILDI VA TIZIMGA ULANDI (Ruslan sorovi: 'bunday hatolar yana bormi, birma-bir tekshirib chiq'). 12-avgustdagi saboq boyicha togri manba ishlatildi: GET /clients/transactions/JsonData?active=Y&access=Y. JAVOB TUZILISHI (2026-08-19 da aniqlangan): {data:[...], currency, currencyNames}, har qator NOMLANMAGAN massiv (indeks 0..27). USTUNLAR: 0/1=client_id, 2=mijoz nomi, 4=aloqa shaxsi, 6=tuman, 7=hafta kuni, 8=manzil, 9=telefon, 10=limit matni, 11=JAMI BALANS (manfiy=qarz) <- KERAKLI RAQAM, 12=qarz qismi, 13 va 16=qoplovchi qismlar, 17=tolov muddati (HTML span ichida, qizil rang), 18=kun soni, 25=agent nomi. ARIFMETIK TASDIQ: 12(-555,533,929) + 13(95,070,500) + 16(22,879,500) = 11(-437,583,929) - ANIQ TOGRI KELADI, yani 11-ustun haqiqiy sof balans. RUSLAN SKRINSHOTI BILAN SOLISHTIRISH: 12-avgustda u -436,590,230 korsatgan edi, bugun -437,583,929 - bir hafta oraliqda ozgargan, MOS. NATIJA (2026-08-19): kochadagi qarz -437,583,929 som, 434 mijozdan 417 tasi qarzdor. Eng kattalari: Uzum Market -19.3 mln (Offis), Uchqun Aka Sam Moyka Chirchik -13.1 mln (Boxodirxoja), Avto Moyka Jamshid Aka -12.0 mln (Angren), Dima Aka Mirobod -10.9 mln (Offis), Javoxir aka -9.9 mln (Boxodirxoja). sd-growth.mjs dagi qarzdorlik() funksiyasi endi shu ustunni ishlatadi, izohda tuzoq hujjatlashtirilgan. ORTACHA CHEK ham tekshirildi: bu oddiy bolish (savdo/buyurtma), ikkala kirish qiymati allaqachon SalesDoc bilan tasdiqlangan, mustaqil manba shart emas. Iyul nazorat nuqtasi: 642,241,500 / 1350 = 475,734 som. XULOSA: savdo, buyurtma, AKB, qarzdorlik, ortacha chek - HAMMASI TEKSHIRILDI VA TASDIQLANDI. Faqat agent intizomi korsatkichlari (bizning kuzatuvimizdan) mustaqil manbaga ega emas - ular Wialon ulangach mashina GPS'i bilan kross-tekshiriladi.

*<- [[hub|Xarita]]*
