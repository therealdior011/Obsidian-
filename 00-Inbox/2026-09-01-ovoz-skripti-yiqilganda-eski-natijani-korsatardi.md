---
type: error
title: ovoz-skripti-yiqilganda-eski-natijani-korsatardi
date: 2026-09-01
status: confirmed
verified: false
---

2026-09-01 XAVFLI XATO TOPILDI VA TUZATILDI. ovoz-matn.py yiqilganda (xotira yetmay 'mkl_malloc: failed to allocate memory') ESKI ovoz-natija.txt joyida qolardi va men uni YANGI transkripsiya deb o'qidim. Bugun aynan shu bo'ldi: Bekzod ikkita YANGI ovoz yubordi (372 KB va 133 KB), skript ikkalasida ham yiqildi, lekin ekranga 30-avgustdagi 66 soniyalik xabarning matni chiqdi. Men buni sezmasam, Bekzodga BUTUNLAY BOSHQA xabarning mazmunini aytgan bo'lardim. TUZATILDI: (1) natija fayli ishdan OLDIN o'chiriladi, (2) xato bo'lsa exit code 1 va aniq xabar, (3) cpu_threads=2, num_workers=1 - xotira kamroq. SABOQ: har qanday 'natija faylga yoziladi' naqshida - eski faylni AVVAL o'chirish shart, aks holda yiqilish jim qolib eski ma'lumot yangi deb uzatiladi. XOTIRA MASALASI: large-v3 int8 uchun ~2.5 GB kerak, tizimda 7.24 GB dan 1.19 GB bo'sh edi. RAG-server (embed_server.py, 689 MB) vaqtincha to'xtatildi -> 1.88 GB bo'ldi -> ishladi. Keyin RAG qaytarildi (PID 20112).

*<- [[hub|Xarita]]*
