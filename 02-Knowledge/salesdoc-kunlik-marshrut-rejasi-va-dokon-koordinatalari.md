---
type: knowledge
title: salesdoc-kunlik-marshrut-rejasi-va-dokon-koordinatalari
date: 2026-08-17
status: confirmed
verified: false
---

2026-08-17 KATTA IMKONIYAT TOPILDI (Ruslan aytdi: 'har bir agentning oz kunlik planlari boladi va salesdoctorda bu royxat bor, dokonlarning haritadagi kordinatalarigacha'). TASDIQLANDI - IKKI MANBA: (1) POST /clients/agentRoute/getClients - 34 ta hudud (territoryId), har birida HAFTA KUNI raqami boyicha (1,2,3,5,6,7) mijoz ID royxati. (2) POST /clients/client/JasonData2/?pageUrl=/clients/client/&active=Y - 2260 ta mijoz, HAR BIRIDA: clientName, firmName, tel, agent (masalan 'Angren & Oqqorgon(Пт)'), day (Пн/Вт/Ср/Чт/Пт/Сб/Вс), city, address, orient, clientCat, LAT, LON, clientId, active. KOORDINATA 2205/2260 = 98% da BOR. Javob hajmi 2.1 MB - toolga sigmaydi, faylga tushadi, python bilan parse qilish kerak. KUNLIK REJA (agent x hafta kuni, koordinatali mijozlar): Muhammad Ali 262 jami (Пн 48), Offis 258 (Сб 105!), Yashnobod & Sergeli 225 (Пт 56), Muhammadjonov 220 (~30/kun bir tekis), Athamov 195, Angren & Oqqorgon 192, Sobitov 177, Sobirov 165, Boxodirxoja 139, Murodullayev 134, Djorayev 111 (Пт va Сб = 0). Yana kichik agentlar bor: Jalilov Ulugbek 15, Qoldoshev Sardor 10, Muhamedova Hamida 2, Mexramova Nigora 1, 'Xodim Kutilmoqda' 1, va agenti korsatilmagan 88 ta. BU NIMA BERADI: endi audit 'rejadagi N dokondan nechtasiga bordi', 'qaysilari tashlab ketildi (nomi/manzili bilan)', 'dokonga haqiqatan yaqin bordimi (GPS vs dokon koordinatasi)', 'marshrut mantiqiymi' degan ANIQ savollarga javob bera oladi - bu '90 daqiqa yoqoldi' degan bilvosita belgidan ANCHA KUCHLIROQ. QOSHIMCHA: /report/workingTime da ham 'План/Посещенные/Не посещенные' ustunlari bor, ikki manbani solishtirib tekshirish mumkin.

*<- [[hub|Xarita]]*
