---
type: fix
title: salesdoc-kunlik-savdo-demo-hisobi-etibordan-chetda-qoldi
date: 2026-08-14
status: draft
verified: false
---

MUHIM XATO (2026-08-13, kechqurun): 13.08 kun yakuni hisobotida savdo summasini /report/visit/getjson'dagi 'buyurtma summasi' maydonidan hisobladim (16.9 mln), lekin Ruslan shubha bildirgach qayta tekshirdim - to'g'ri raqam 28,123,000 so'm ekan (52 buyurtma, PowerShell orqali xom /orders/list/orders ma'lumotidan ConvertFrom-Json bilan aniq hisoblab). SABAB: 'Demo' nomli maxsus/tizim hisobi orqali kiritilgan buyurtmalar (11,224,000 so'm, ehtimol ofis yoki katta hajmli alohida buyurtmalar) na mening qo'lda agent-nom qidiruvimda (faqat 9 ta ma'lum dala agenti nomini qidirgan edim), na tashrif-hisobotida (Demo uchun 'vizit' yozuvi yo'q ko'rinadi) aks etmagan. SABOQ: (1) kunlik savdo hisoblashda faqat ma'lum agent nomlarini emas, BARCHA created_by qiymatlarini (shu jumladan 'Demo', 'Offis' kabi tizim hisoblarini) hisobga olish kerak; (2) eng ishonchli usul - tashrif-hisobotidagi summa emas, to'g'ridan-to'g'ri /orders/list/orders'dagi 'sales' massivini (mahsulot qatorlari) yig'ish, buni PowerShell'da ConvertFrom-Json orqali qilish tezroq va aniqroq (escaped-JSON formatida qaytganda ayniqsa qo'l bilan grep qilishdan ko'ra); (3) agar raqam kutilganidan sezilarli farq qilsa va egasi shubha bildirsa - darhol muqobil, mustaqil usul bilan qayta tekshirish kerak, o'zini oqlashga urinmasdan.

*<- [[hub|Xarita]]*
