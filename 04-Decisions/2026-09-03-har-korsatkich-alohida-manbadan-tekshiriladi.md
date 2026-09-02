---
type: decision
title: har-korsatkich-alohida-manbadan-tekshiriladi
date: 2026-09-03
status: confirmed
verified: false
---

2026-09-02 RUSLAN TALABI (aynan): 'malumotlarni alohida har bir kriteriya boyicha olib kelinib tekshiri olinishi shart'. QURILDI: hisobot-tekshiruv.mjs - har ko'rsatkichni IKKI MUSTAQIL yo'l bilan olib solishtiradi, 0.5% dan katta farq bo'lsa 'FARQ' deb belgilanadi. TEKSHIRUVLAR: (1) Savdo - buyurtma qatorlari yig'indisi vs /dashboard/sales sahifasining o'z summasi; (2) Buyurtma soni - buyurtma ro'yxati vs sotuv qatorlaridagi turli order_id; (3) Kassa - agent qatorlari yig'indisi vs jadvalning 'Итого' qatori; (4) Qarzdorlik - /clients/computation/debtApi vs /clients/transactions/JsonData balanslari (IKKI BOSHQA endpoint); (5) Ombor qoldig'i - mahsulot qatorlari vs kategoriya jamlanmalari; (6) Xarid qilgan do'kon - buyurtmalardagi turli mijoz vs sahifadagi rayon kesimi AKB ustuni. NATIJA (2026-09-02 va 2026-08-31 da sinaldi): oltalasi ham MOS. Savdo/buyurtma/kassa/ombor/do'kon - farq 0; qarzdorlikda 200 000 farq (447 mln dan 0.04%, chegara ichida). ULANDI: kunlik hisobot rasmiga alohida 'Tekshiruv' jadvali qo'shildi - raqam bilan birga uning manbasi va tekshirilgani ko'rinadi. Tekshiruv yiqilsa hisobot BARIBIR ketadi (nazorat vositasi, to'siq emas). XATO QILDIM VA TUZATDIM: birinchi urinishda 'xarid qilgan do'kon' tekshiruvida sahifa ustunini TAXMIN qilib eng kichik sonni olgandim va 1021 chiqdi (bu OKB - bazadagi jami do'kon edi, AKB emas). Har safar yolg'on ogohlantirish beradigan tekshiruv zararli - ustun tartibi sahifadan aniqlanib tuzatildi. SABAB: 2026-09-01 da hududiy va yillik hisobot bir xil ma'lumotdan 22.8 mln farq bergan va buni RUSLAN sezgan, men emas.

*<- [[hub|Xarita]]*
