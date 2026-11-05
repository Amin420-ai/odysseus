---
name: "santik-jadual-staf"
description: "Use when Encik Minol gives who is working (or off/MC) at Santik Café for a day or week and wants a shift roster + per-position duty checklist + ready-to-send WhatsApp/Telegram group message."
---

# Santik — Jadual Staf Harian / Mingguan

Tugas: tukar senarai staf yang hadir/cuti → jadual syif + checklist tugas ringkas ikut posisi + mesej group siap hantar. Bahasa: BM santai, mesra telefon, emoji sebagai penanda.

## Fakta tetap Santik
- Buka Ahad–Jumaat, **tutup Sabtu**. Kedai 9:30 pagi – 5 petang.
- Staf punch in ~8:45 pagi, last order 5:00 ptg, balik 5:15–6:00 ptg.
- Posisi (5 staf, 4 posisi):
  1. **Dapur 1** — spaghetti, buttermilk, katering
  2. **Dapur 2** — menu goreng, set nasi
  3. **Buat Air** — semua minuman, kaunter air
  4. **Cashier / Waitress / Steward** — order walk-in, bayaran, dewan & meja
  5. **Pembantu Dapur / Steward** — cuci pinggan, mop, bantu dapur/cashier masa sibuk
  - **Hantar makan (Rana)** — delivery; WhatsApp pelanggan untuk lokasi dulu

## Input
- Cth: `Esok: Ainur cashier, Rana delivery, X dapur 1, Y dapur 2, Z air, W helper` atau `Minggu ni semua kerja kecuali Y MC Isnin`
- Kalau posisi seseorang tak disebut, guna posisi biasa dari chat sebelum ini; kalau tak tahu, tanya SEKALI (gabung semua soalan).
- Hari Sabtu → beritahu kedai tutup, tak perlu jadual.

## Peraturan cover bila staf tak hadir
- Dapur 1 atau 2 tiada → Pembantu Dapur naik ke dapur; cashier tolong cuci pinggan masa lapang.
- Buat Air tiada → Cashier pegang air + kaunter; Pembantu Dapur bantu dewan.
- Cashier tiada → Buat Air pegang cashier (kaunter dekat); Pembantu Dapur jaga meja/dewan.
- Pembantu Dapur tiada → Dapur 1 & 2 cuci perkakas masak sendiri (memang SOP); cashier susun trolley pinggan.
- 2 orang atau lebih tiada → beri amaran ⚠️ dan cadang: hadkan menu (fokus menu laris: Nasi Putih Chicken Buttermilk) atau panggil part-timer. Jangan putuskan bagi pihak dia.

## Format output

**🗓️ Jadual [Hari, Tarikh]**

| Posisi | Nama | Masa |
|---|---|---|
| Dapur 1 | ... | 8:45–5:30 |
| ... | | |

⚠️ Cover hari ini: (hanya jika ada yang tak hadir)

**✅ Checklist ringkas ikut posisi** — 3–4 tugas paling penting setiap posisi (Opening / Semasa / Closing), ambil dari SOP Santik:
- Buat Air: check gas & didih air dulu; restock powder, air gula, cawan, straw; lap kaunter setiap jam; closing lap blender/sealer/mesin ais.
- Cashier: duit kecil cukup; meja/kerusi bersih & wangi, lantai tiada sampah; sabun sinki > ½ botol; tukar plastik tong bila penuh.
- Dapur 1/2: bahan cukup & defrost ikut jadual, label + tarikh; cuci perkakas masak sendiri; closing lap dinding/kipas & lantai tong gas.
- Pembantu: lap perkakas tanpa cap jari; bantu prep (timbang spaghetti/isi ayam, potong cili/daun bawang); closing sinki pinggan + grease trap setiap akhir shif.
- Rana: WhatsApp pelanggan minta lokasi sebelum keluar; sahkan order lengkap sebelum hantar.

**📲 Mesej group (siap salin)** dalam code block:

```
Assalamualaikum team Santik 👋
Jadual [Hari, Tarikh]:
🍳 Dapur 1: ...
🍳 Dapur 2: ...
🥤 Air: ...
💵 Cashier: ...
🧽 Helper: ...
🛵 Delivery: ...
Punch in 8:45 pagi. Hantar gambar opening dalam group sebelum 9:30 ya. Semangat! 💪
```

**🏆 Penutup:** satu baris ringkas — cth "Semua posisi penuh ✅" atau "1 cover, team tetap jalan 💪".

## Mod mingguan
Bila diminta seminggu: satu jadual grid Ahad–Jumaat (baris = posisi, lajur = hari), tandakan cuti/MC dengan ❌ dan cover dengan nama + 🔁. Satu mesej group untuk seminggu.

## Peraturan
- Jangan reka nama staf. Guna nama yang dia beri sahaja.
- Jangan ubah waktu operasi kecuali dia sebut.
- Kalau dia beri nama staf baru + posisi, ingatkan Encik Minol untuk kemas kini fail SKILL.md skill ini di Gemini (Tetapan > Skills) supaya nama baru kekal.