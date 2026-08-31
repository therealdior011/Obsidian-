---
type: project
title: AI ombor agenti
date: 2026-08-30
status: confirmed
verified: false
---

2026-08-30 QURILDI VA ISHGA TUSHDI. Fayllar: ombor-qoldiq.mjs (qoldiq parseri), ombor-savdo.mjs (dona hisobi), ombor-agent.mjs (mantiq), ombor-rasm.mjs (rasm+yuborish), ombor-obsidian.mjs (vaultga yozish), ombor-listener.mjs + supervisor (alohida bot @hoffen_ombor_managerbot). Vazifa SD-OmborZakaz har dushanba 09:00. MANTIQ: 30 kun savdo/30 = kunlik sarf, x40 = kerak, qoldiq ayriladi, blok karraligiga yaxlitlanadi. TEKSHIRILGAN FAKTLAR: (1) /stock/stock/detail sahifasida UCHTA table bor, haqiqiysi faqat id=list-table, qolgan ikkitasi yashirin shablon - umumiy MCP parseri uchalasini qaytarib ustunlarni siljitadi, shuning uchun alohida parser yozildi. (2) thead 18 ta th, qatorda 15 katak (oxirgi 3 sarlavha colspan=2) - sarlavha soniga qarab moslash XATO. (3) Jadvalda kategoriya jamlanma qatorlari ham bor, farqi: kategoriyada '#' ustuni raqamlangan. Tekshirdim: 12 kategoriyaning hammasi bolalari yig'indisiga aniq teng. (4) product_id ombor va /orders/list/orders da BIR XIL - 129 ta sotilgan mahsulotning hammasi mos keldi, 0 nomuvofiqlik. (5) MAVSUMIYLIK: avgustda antifriz sotilmaydi va 'harakatsiz' ro'yxatiga tushadi - yanvar savdosi bilan tekshirildi, 51 tadan 25 tasi qishda sotilgan, ular ajratildi. NATIJA 29-avgust: 222 mahsulot, qoldiq 44667 dona (asosiy omborda 30234), 30 kunda 55448 dona sotilgan, 57 ta mahsulotga zakaz kerak, 6 tasi tugagan. Eng kattasi GRAFF Antifreeze -40 QIZIL 1kg: 1930 sotilgan, 418 qolgan, 6 kun, zakaz 2160. BAZA XATOSI TOPILDI: 'KALKULYATOR' (100) va 'Kalkulyator' (89) - bitta tovar ikki nomda.

*<- [[hub|Xarita]]*

## 2026-08-30 - qo'shimcha
2026-08-30 KENGAYTIRILDI - bot endi jonli savol-javob beradi (ombor-javob.mjs). Buyruqlar: /zakaz (rasm hisobot), /tugagan, /harakatsiz, yoki mahsulot nomi. Ruxsat faqat Ruslan va Bekzodga - ombor raqamlari ichki ma'lumot. Kesh 30 daqiqa (hisobla() beshta SalesDoc so'rovi yuboradi). QIDIRUV TUZOG'I: mahsulot nomlari aralash kirill-lotin ('HOFFEN1 жидкость сухой туман'), Ruslan lotinchada 'tuman' deb yozadi va birinchi sinovda 1 ta topgan, aslida 89 ta bor. Kirilldan lotinga translit qo'shildi - endi 'tuman' 89, 'zamerzayka' 24, 'ochistitel' 5 topadi.

## 2026-08-30 - qo'shimcha
2026-08-30 OYLIK REJA MODULI qo'shildi: ombor-oylik-reja.mjs + ombor-reja-rasm.mjs. Ruslan savoli 'asosiy omborda nima yo'q va sentabrga qancha tayyorlash kerak'. MANTIQ: o'tgan oy savdosi x MAVSUM NISBATI (o'tgan yilning shu ikki oyi taqqoslashidan, KATEGORIYA kesimida) = kutilgan savdo, undan ASOSIY OMBOR qoldig'i ayriladi, blok karraligiga yaxlitlanadi. Kam ma'lumotli kategoriyada (30 donadan kam) tuzatish qo'llanmaydi. NATIJA sentabr-2026: 78 ta mahsulot, 29997 dona (asosiy ombor bo'yicha) yoki 16983 (hamma ombor hisobga olinsa - pastki chegara). Ikkalasi ham ko'rsatiladi. Eng kattalari: qog'oz 22000, Antifreeze QIZIL 2370, KO'K 1935, nezamerzayka OKEAN 1032. Ishlatish: node ombor-reja-rasm.mjs 2026-09 [--yubor]
