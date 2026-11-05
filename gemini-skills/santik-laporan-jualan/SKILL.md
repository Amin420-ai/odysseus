---
name: "santik-laporan-jualan"
description: "Laporan jualan harian Santik Café (UUM). Guna bila Pkin/Encik Minol tampal atau muat naik data jualan hujung hari dari POS Chupjer (screenshot, salinan teks, CSV) atau sebut 'laporan jualan', 'sales hari ni', 'closing report'. Hasilkan ringkasan BM siap hantar ke WhatsApp."
---

# Santik Café — Laporan Jualan Harian

Santik Café buka Ahad–Jumaat (Sabtu tutup), 9:30 pagi – 5 petang, Pusat Islam UUM. Selepas tutup, Encik Minol beri data jualan dari POS Chupjer (screenshot, tampal teks, atau fail). Dia guna telefon dan tak pandai kod. Matlamat: **hantar data → dapat laporan → salin ke WhatsApp.**

## Langkah
1. Baca semua data yang diberi. Tarikh: guna tarikh dalam data; kalau tiada, tanya SEKALI.
2. Semak: jumlah ikut kaedah bayaran ≈ jumlah jualan (beza ≤ RM1); kalau tak padan, beritahu beza dalam satu baris, jangan sorok.
3. Jangan reka nombor. Kalau sesuatu tak ada dalam data (contoh waktu order), langkau bahagian itu.
4. Kalau screenshot kabur, sebut nombor mana yang tak jelas dan minta ambil gambar semula bahagian itu sahaja.
5. Sasaran harian: tanya SEKALI kalau belum diberitahu (contoh RM1,300). Kalau tiada, siapkan laporan tanpa bahagian sasaran.
6. Banding dengan semalam dan hari yang sama minggu lepas hanya jika Encik Minol beri angka itu dalam chat.

## Format laporan (dalam code block, siap salin)
```
📊 LAPORAN JUALAN — [Hari, Tarikh]
💰 Jumlah jualan: RM[x]   [🎯 CAPAI / belum capai sasaran RM[y] — [z]%]
🧾 Order: [n]  |  Purata sebil: RM[x]
💳 Bayaran: Tunai RM[a] · QR RM[b] · Kad RM[c]
🏆 Top 5 menu:
1. [menu] — [qty] (RM[x])
...
⏰ Waktu puncak: [jam] ([n] order)
📈 vs semalam: [+/-RM, %]   vs [hari] minggu lepas: [+/-RM, %]
🔥 Streak capai sasaran: [n] hari
💡 [satu cadangan ringkas untuk esok berdasarkan data]
```
Bar kemajuan sasaran: guna 10 petak, contoh 🟩🟩🟩🟩🟩🟩🟩⬜⬜⬜.

## Tracker
Gemini tak boleh kemas kini Excel sendiri. Selepas laporan, beri SATU baris siap tampal untuk Google Sheet tracker Encik Minol, lajur dipisah tab:
`Tarikh | Jumlah | Order | Tunai | QR | Kad | Menu #1`
Ingatkan dia tampal baris itu di hujung tab "Harian".

## Gaya
BM santai (rojak OK), pendek, mesra telefon. Headline nombor dan status sasaran di atas. Tiada penjelasan panjang.

## Kes khas
- Hari tiada jualan / Sabtu: sahkan sahaja, tiada laporan.
- Jika Encik Minol tampal beberapa hari tracker dan tanya "minggu ni macam mana": ringkaskan jumlah minggu, hari terbaik, bilangan hari capai sasaran.
