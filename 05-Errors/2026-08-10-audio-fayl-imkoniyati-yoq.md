---
type: fix
title: audio-fayl-imkoniyati-yoq
date: 2026-08-10
status: confirmed
verified: true
---

Ruslan 1 soatlik audio yozuv (.m4a, 33.5MB) yubordi va 'eshitib chiq' deb so'radi. IKKI cheklov aniqlandi: 1) Telegram bot API 20MB dan katta faylni yuklab bera olmaydi (download_attachment xato qaytardi: 'file is too big'), 2) hatto yuklab olinsa ham, hozirgi vositalar orasida audio transkripsiya/tinglash imkoniyati yo'q (faqat matn/rasm/PDF o'qiladi). Ruslanga ochiq tan olindi. Kelajakda audio so'ralsa - avval fayl hajmini tekshirish (20MB chegarasi) va transkripsiya vositasi yo'qligini eslatish kerak, vaqt sarflab qayta urinmaslik uchun.

---

## YANGILANDI 2026-08-30 — endi ovoz eshitiladi

Yuqoridagi "transkripsiya vositasi yoq" degan xulosa ESKIRDI.

ORNATILGAN: faster-whisper, `C:/Users/user/.assistant/scripts/ovoz-matn.py`.
Ishlatish: `OVOZ_MODEL=large-v3 venv/Scripts/python.exe scripts/ovoz-matn.py <fayl.oga> uz`
Natija `ovoz-natija.txt` ga UTF-8 da yoziladi (konsolga chiqarish cp1251 da yiqiladi).

MODEL TANLASH — MUHIM, tekshirilgan:
- `small` — ozbekchani BUTUNLAY buzadi. Namuna: "Bida che, mitihaled bar, bu umumi skilet teksher watde" — manosiz tovushlar, model oylab topgan. ISHLATMASLIK KERAK.
- `large-v3` — 3.09 GB, ozbekchani QISMAN oladi. Mukammal emas, lekin MANO CHIQADI.
  Namuna: "mitti xalad bar, bu umumi sqilat teksir vatdi, hadimlani masinasi deyan bar bogan maqsulatlani xoshib teksir vatdi"
  = "bitta xato bor, umumiy skladni tekshiribdi, xodimlarning mashinasidagi mahsulotlarni ham qoshib tekshiribdi".

TUZOQ: large-v3 keshda YARIM turgan bolishi mumkin — faqat tokenizer/config tushib, model.bin `.incomplete` holatda qoladi. 25-avgustda aynan shunday bogan va "yuklandi" deb oylab, aslida kichik model ishlatilgan. Tekshirish: blobs papkasida `.incomplete` fayl bormi. Yuklash: `snapshot_download("Systran/faster-whisper-large-v3", max_workers=4)`.

QOIDA: transkripsiya natijasini HAQIQAT deb bermaslik. Tushunilgan manoni ochiq "ishonchsiz, tasdiqlang" deb belgilab, yuboruvchidan tasdiq sorash. 2026-08-30 da shunday qilindi va togri chiqdi.

20 MB cheklovi hamon kuchda (Telegram bot API) — 1 soatlik yozuv baribir yuklanmaydi.

*<- [[hub|Xarita]]*
