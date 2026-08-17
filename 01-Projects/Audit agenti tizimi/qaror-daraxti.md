---
type: knowledge
title: Audit agenti — qaror daraxti
date: 2026-08-17
status: draft
verified: false
---

# Audit agenti — qaror daraxti

Bu tizim har bir qadamda qanday qaror qabul qilishini ko'rsatadi.
Manba: [[Audit agenti tizimi]] · [[salesdoc-report-workingTime-itogi-vizitov-manbasi]] · [[salesdoc-kunlik-marshrut-rejasi-va-dokon-koordinatalari]]

---

## 1. Ertalabki chiqish (07:00–12:00, har 15 daqiqa)

```mermaid
flowchart TD
    A["Har 15 daqiqada<br/>SD-MorningWatch"] --> B{"GPS signali<br/>60 daqiqadan yangimi?"}

    B -->|"Yo'q"| C["Holat: signal eski<br/>GPS bo'yicha xulosa YO'Q"]
    C --> C1{"SalesDoc'da<br/>sinxronizatsiya bormi?"}
    C1 -->|"Ha"| C2["Zaxira o'lchov:<br/>1-sinxronizatsiya + 1-tashrif"]
    C1 -->|"Yo'q"| C3["Aniqlay olmadim<br/>hisobotda shunday yoziladi"]

    B -->|"Ha"| D{"Bazadan masofa<br/>100 metrdan kammi?"}

    D -->|"Ha - bazada"| E{"Soat 09:00 dan<br/>o'tdimi?"}
    E -->|"Yo'q"| E1["Normal - kutamiz"]
    E -->|"Ha"| F["15 daqiqa sanoq<br/>boshlandi"]
    F --> G{"09:15 da hali<br/>bazadami?"}
    G -->|"Yo'q - chiqdi"| H
    G -->|"Ha"| I{"Sotuv boshlandimi?<br/>(tashrif bor)"}
    I -->|"Ha"| E1
    I -->|"Yo'q"| J["QOIDA BUZILDI<br/>ogohlantirish oqimiga"]

    D -->|"Yo'q - tashqarida"| H{"Oldingi tekshiruvda<br/>bazada edimi?"}
    H -->|"Ha"| K["CHIQISH VAQTI qayd etildi"]
    H -->|"Yo'q"| L["Marshrutda<br/>yoki bazaga kelmagan"]

    style J fill:#ffe0e0,stroke:#c00
    style K fill:#e0ffe0,stroke:#0a0
    style C3 fill:#fff3d0,stroke:#c90
```

---

## 2. Kun ichida yo'qolish

```mermaid
flowchart TD
    A["Tashriflar jurnali<br/>/report/visit/getjson"] --> B["Ketma-ket tashriflar<br/>orasidagi tanaffus"]
    B --> C{"Tanaffus<br/>90 daqiqadan uzunmi?"}
    C -->|"Yo'q"| D["Normal"]
    C -->|"Ha"| E{"Vaqt 13:00-14:00<br/>oralig'idami?"}
    E -->|"Ha"| F["Tushlik - hisobga olinmaydi"]
    E -->|"Yo'q"| G{"Bugun rejadagi<br/>do'konlar tugaganmi?"}
    G -->|"Ha"| H["Ish tugagan - normal"]
    G -->|"Yo'q"| I["QOIDA BUZILDI<br/>ogohlantirish oqimiga"]

    style I fill:#ffe0e0,stroke:#c00
    style F fill:#e8e8e8
```

---

## 3. Ogohlantirish va shtraf (7 kunlik oyna)

```mermaid
flowchart TD
    A["Qoida buzildi"] --> B{"Dedup: shu agent<br/>shu sabab bilan<br/>bugun ogohlantirilganmi?"}
    B -->|"Ha"| C["Jim - takror yubormaymiz"]
    B -->|"Yo'q"| D{"Sinov davri<br/>tugadimi?<br/>(birinchi 2 hafta)"}

    D -->|"Yo'q"| E["Faqat yoziladi<br/>xabar YUBORILMAYDI"]
    D -->|"Ha"| F{"7 kunda nechinchi<br/>marta?"}

    F -->|"1-marta"| G["Agentning o'ziga xabar<br/>Sotuvga qayting"]
    F -->|"2-marta"| H["Agentga xabar<br/>+ guruhga qator"]
    F -->|"3-marta"| I["SHTRAF TAKLIFI<br/>Ruslan akaga"]
    F -->|"4+ marta"| J["Tizimli muammo<br/>suhbat kerak"]

    I --> K{"Ruslan aka<br/>tasdiqladimi?"}
    K -->|"Ha"| L["Shtraf yoziladi<br/>guruhga hisobot"]
    K -->|"Yo'q"| M["Hisoblagich nolga<br/>tushadi"]

    style I fill:#fff3d0,stroke:#c90
    style L fill:#ffe0e0,stroke:#c00
    style E fill:#e8e8e8
    style C fill:#e8e8e8
```

---

## 4. Marshrut bajarilishi (kun oxiri)

```mermaid
flowchart TD
    A["Bugungi reja<br/>agentRoute + mijoz koordinatalari"] --> B["Rejadagi do'konlar soni"]
    B --> C["Tashrif qilinganlar<br/>/report/visit/getjson"]
    C --> D{"Tashlab ketilgan<br/>do'kon bormi?"}
    D -->|"Yo'q"| E["Reja bajarildi"]
    D -->|"Ha"| F["Ro'yxat: nomi + manzili"]
    F --> G{"Agent o'sha do'kon<br/>yonidan o'tganmi?<br/>(GPS vs koordinata)"}
    G -->|"Ha"| H["Yonidan o'tdi,<br/>lekin kirmadi"]
    G -->|"Yo'q"| I["Umuman bormadi"]

    style H fill:#ffe0e0,stroke:#c00
    style E fill:#e0ffe0,stroke:#0a0
```

---

## Qaror nuqtalarining sozlamalari

Bularning hammasi `sd-run.mjs` ichidagi `QOIDALAR` blokida, bitta joyda:

| Sozlama | Hozirgi qiymat | Izoh |
|---|---|---|
| Baza radiusi | 100 m | `.env` da `BAZA_RADIUS_M` |
| Chiqish muddati | 09:00 + 15 daq | Ruslan belgilagan |
| Signal eskirish | 60 daqiqa | Undan eski = "aniqlay olmadim" |
| Yo'qolish chegarasi | 90 daqiqa | **Kalibrlash kerak** — hozir juda past |
| Tushlik | 13:00–14:00 | Hisobga olinmaydi |
| Dedup oynasi | 3 kun | Takror xabar to'xtatiladi |
| Shtraf chegarasi | 7 kunda 3 marta | Ruslan tasdig'i bilan |
| Sinov davri | 2 hafta | Bu davrda xabar yuborilmaydi |

> **Diqqat:** 90 daqiqalik chegara hozirgi ma'lumotda 8 kunda 7 ta agentni "3+ marta" ga chiqaradi.
> Sinov davridan keyin qayta kalibrlanadi — maqsad: kuniga 2–3 ta haqiqiy holat, 30 ta emas.
