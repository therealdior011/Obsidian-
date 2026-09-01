---
type: decision
title: xodimlar-yillik-hisoboti-savdo-kassa-kochada
date: 2026-09-01
status: confirmed
verified: false
---

2026-09-01 Ruslan so'radi: har savdo xodimi bo'yicha 2026 yillik hisobot - Savdo / Kassa / Ko'chada qoldiq, rasmda grafik bilan. QURILDI: hisobot-yillik-xodim.mjs (ma'lumot) + hisobot-yillik-rasm.mjs (rasm+grafik). YANGI MANBA TOPILDI: /dashboard/kassaIncome?datestart=&endstart=&filter=Фильтр - sahifada id='agent1' jadvali AGENT KESIMIDA kassa beradi, ustunlar: ИД агента, Название, Наличный Сум, Безналичный Сум, перечисления. Bu ilgari ishlatilmagan edi. Kassa = uchalasining yig'indisi. QOLDIQ: /clients/transactions/JsonData, 11-ustun sof balans (manfiy=qarz), 25-ustun agent nomi. MUHIM QAROR: ko'chadagi qoldiqni 'savdo minus kassa' deb hisoblash NOTO'G'RI - u yil boshidagi qarzni hisobga olmaydi. Uchala raqam ALOHIDA o'lchandi, biri ikkinchisidan chiqarilmadi. Ruslanga bu ochiq aytildi (u misolda 70-65=5 degan edi). IKKI TUZOQ TOPILDI VA TUZATILDI: (1) ba'zi buyurtmalarda created_by NOM emas LOGIN RAQAMI ('d0_192') - agent_id orqali kassa jadvalidagi id->nom xaritasidan hal qilinadi, aks holda Jalilov Ulug'bek ikki qator bo'lib ko'rinardi; (2) mijoz bir necha agentga biriktirilgan bo'lsa nomlar vergul bilan yopishadi ('Offis,Muhammad Ali') - birinchisi olinadi. NATIJA (2026-01-01..09-01, dala agentlari): savdo 4262.3 mln, kassa 4032.1 mln, ko'chada 344.3 mln, yig'ilgan 95%. Eng yaxshi Athamov 99%, eng past Sobitov 76%. Ofis hisoblari (Demo 813 mln savdo/0 kassa, Offis 6 mln savdo/773 mln kassa) ALOHIDA jadvalda - markazda qabul qilingan to'lovlar o'sha yerga yoziladi.

*<- [[hub|Xarita]]*
