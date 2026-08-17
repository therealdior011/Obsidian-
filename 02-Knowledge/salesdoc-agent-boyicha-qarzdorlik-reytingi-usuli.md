---
type: knowledge
title: salesdoc-agent-boyicha-qarzdorlik-reytingi-usuli
date: 2026-08-17
status: confirmed
verified: false
---

2026-08-17: Ruslan /clients/transactions ni korsatib 'savdo xodimlarini qarzdorlik reytingini tuzib ber' dedi. MUAMMO: /clients/transactions/JsonData?active=Y&access=Y JSON emas HTML content-type bilan qaytadi va MCP uni KESIB tashlaydi (length/start/draw parametrlari ISHLAMAYDI, ayni natija qaytadi). ISHLAGAN YOL (2 ta manbani birlashtirish): (1) GET /clients/computation/debtApi?page=1&limit=2000 -> {status, meta{total_count}, data[]} har mijoz uchun: customer_id, customer_name, total_debt, debt_0_to_7_days, debt_8_to_15_days, debt_16_to_30_days, debt_31_to_60_days, debt_61_to_90_days, debt_over_90_days. AGENT MAYDONI YOQ. (2) POST /clients/client/JasonData2/?pageUrl=/clients/client/&active=Y -> 2261 mijoz, maydonlar: clientId, clientName, agent, city, lat, lon va h.k. BOGLASH: id prefikslari HAR SOROVDA BOSHQACHA (debtApi da 'f4_5667', mijozlarda 'a7_10') - pastki chiziqdan KEYINGI raqam boyicha birlashtiriladi, prefiks tashlanadi. NATIJA (2026-08-17): jami 779 532 280 som, 566 mijoz. Reyting: Offis 164.5 mln (48 mijoz, >30kun 79.7 mln, >90kun 22.9 mln - eng xavfli), Athamov 99.2, Muhammad Ali 82.2, Boxodirxoja 80.4, Angren&Oqqorgon 75.7 (qarzning 47% i muddati otgan - eng yomon nisbat), Sobirov Botirjon 59.6 (eng yaxshi nisbat, 20%), Murodullayev 56.3, Yashnobod&Sergeli 50.5 (57% muddati otgan), Djorayev 47.4 (25 mijozda, ortacha 1.9 mln - eng yuqori), Muhammadjonov 32.1, Sobitov 29.4. CHEKLOV RUSLANGA AYTILDI: bu 'Dolgi po zakazam' manbasidan, u korsatgan Transactions sahifasining 'balans' ustuni oldindan tolovlarni ayiradi - ayrim mijozlarda farq bolishi mumkin. 5 mijoz (528 000) mijozlar royxatidan topilmadi. 'Offis' savdo xodimi emas - ofisga biriktirilgan mijozlar.

*<- [[hub|Xarita]]*
