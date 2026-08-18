---
type: knowledge
title: Audit agenti — tizim xaritasi
date: 2026-08-18
status: confirmed
verified: true
---

# Audit agenti — nimalar qurilgan

Holat: 2026-08-18. Barchasi jonli tekshirilgan.
Papka: `C:\Users\user\.assistant\sd-pipe\`

---

## 1. MCP — tashqi tizimlarga ulanish

| Nomi | Nima beradi | Holat |
|---|---|---|
| **salesdoc** | Savdo tizimi: tashriflar, buyurtmalar, mijozlar, reja, telefon GPS'i | ✅ Ishlayapti |
| **telegram** | Ruslan bilan aloqa, hisobot yuborish | ✅ Ishlayapti |
| **obsidian** | Xotira vault'iga yozish/o'qish | ✅ Ishlayapti |
| **playwright** | Brauzer (Wialon token olishda ishlatildi) | ✅ Ishlayapti |
| **context7** | Texnik hujjatlar | ✅ Ishlayapti |

**Wialon** — MCP emas, to'g'ridan-to'g'ri modul (`wialon.mjs`), chunki faqat 3 ta funksiya kerak.

---

## 2. TOOLS — o'zimiz yozgan modullar

### Ma'lumot olish (1-qatlam: manba)

| Fayl | Vazifasi |
|---|---|
| `wialon.mjs` | Mashina GPS: `login()`, `mashinalar()`, `trek()`. 10 ta Damas, har 2 daqiqada nuqta |
| `sd-metrics.mjs` | SalesDoc: tashrif, GPS, agent ko'rsatkichlari — raqamni **kod** hisoblaydi |
| `sd-route.mjs` | Kunlik marshrut rejasi: qaysi do'konga borishi kerak edi, bordi/bormadi |

### Kuzatuv (jonli)

| Fayl | Vazifasi | Chastota |
|---|---|---|
| `sd-morning.mjs` | Bazadan chiqish vaqti (100 m radius) | har 15 daq, 07:00–12:00 |
| `sd-store-watch.mjs` | Do'konga kirish/chiqish, davomiyligi | har 10 daq, 07:00–22:00 |

### Qaror va hisobot

| Fayl | Vazifasi |
|---|---|
| `sd-run.mjs` | Qoidalar, chegaralar, takror xabarni to'xtatish (dedup) |
| `sd-format.mjs` | Hisobot matni — faqat tayyor raqamdan, raqamga tegmaydi |
| `sd-audit-report.mjs` | Kunlik hisobot yig'ib, 3 manzilga yuboradi |

### Ogohlantirish va tasdiq

| Fayl | Vazifasi |
|---|---|
| `sd-ask.mjs` | Guruhga HA/YO'Q tugmali so'rov yuboradi |
| `sd-listener.mjs` | Tugma bosilishini eshitadi (faqat Ruslan/Bekzod bosa oladi) |
| `sd-sorov-eslatma.mjs` | 30 daqiqa javobsiz qolsa Ruslanga eslatma |

### Nazorat

| Fayl | Vazifasi |
|---|---|
| `sd-watchdog.ps1` | Hisobot kelmasa Ruslanga xabar. Batareya sozlamasi buzilmaganini ham tekshiradi |
| `sd-listener-supervisor.ps1` | Listener yiqilsa 10 soniyada qayta ko'taradi |

---

## 3. HOOKS — avtomatik ishga tushirish

### Task Scheduler

| Vazifa | Vaqti | Holat |
|---|---|---|
| `SD-MorningWatch` | har 15 daq, 07:00–12:00 | ✅ |
| `SD-StoreWatch` | har 10 daq, 07:00–22:00 | ✅ |
| `SD-AuditReport` | 12:30 va 20:00 | ✅ |
| `SD-SorovEslatma` | har 15 daq | ✅ |
| `SD-Watchdog` | 10:00 va 23:00 | ✅ |
| `SalesDoc-DailyReport` | 09:00 | ✅ |
| `SalesDoc-EveningReport` | 22:00 | ✅ |
| `SalesDoc-MonthlyReport` | 22:30 | ✅ |

### Startup papkasi (logonda)

- `SD-ListenerBridge.lnk` → tugma javoblarini eshituvchi, alohida jarayon
- `AssistantRAG.vbs` → xotira qidiruv serveri
- `TelegramListener.lnk` → Telegram aloqasi

### Sessiya hooklari

- `UserPromptSubmit` → har savolda vault'dan tegishli xotirani qo'shadi
- `Stop` → har javobdan keyin "xotiraga yozish kerakmi?" deb eslatadi

---

## 4. SKILLS — ish uslublari

| Skill | Qachon ishlaydi |
|---|---|
| `grilling` | Katta qaror qurishdan oldin savol-javob (audit tizimi shu bilan qurildi) |
| `odam-dosye` | Agent haqida savol berilganda |
| `hisobot` | Hafta/oy yakuni |
| `moliya-nazorat` | Pul, xarajat |
| `qaror-yordam` | "Arziydimi" turidagi savollar |
| `vazifa-nazorat` | Topshiriqlar holati |
| `kunlik-brifing` | Ertalabki xulosa |
| `yigilish`, `hujjat-tayyorlash` | Uchrashuv, hujjat |
| `find-skills` | Yangi skill qidirish |

---

## 5. MA'LUMOT FAYLLARI

| Fayl | Nima saqlaydi |
|---|---|
| `sd-morning.jsonl` | Ertalabki kuzatuv tarixi |
| `sd-store-visits.jsonl` | Do'kon kirish/chiqish voqealari |
| `sd-store-watch-state.json` | Har agentning joriy holati |
| `sd-audit-state.jsonl` | Kunlik audit suratlari |
| `sd-alerts.json` | Takror ogohlantirishni to'xtatish tarixi |
| `sd-sorovlar.jsonl` | HA/YO'Q so'rovlari va javoblari |
| `sd-state.jsonl` | Kunlik ko'rsatkichlar (trend uchun) |
| `.env` | Kalitlar (Telegram bot, Wialon token, baza koordinatasi) |

---

## Hali qurilmagan

1. **Wialon trekini kuzatuvga ulash** — modul tayyor, lekin har 30 daqiqada trek yig'ish hali yozilmagan
2. **Mashina ↔ agent bog'lanishi** — qaysi Damas kimda ekani noma'lum
3. **Ikki manbani solishtirish** — Wialon "do'konda emas" + SalesDoc "tashrif yozilgan" = soxta tashrif signali
4. **Chegaralarni kalibrlash** — 100 m radius, 90 daqiqa to'xtash chegarasi hali haqiqiy ma'lumotda sinalmagan
5. **Agentlarga xabar** — ataylab o'chiq (sinov davri)
