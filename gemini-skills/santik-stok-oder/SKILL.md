---
name: "santik-stok-oder"
description: "Use when Encik Minol sends Santik Café's remaining stock (text, voice or photo) and wants a daily stock status + supplier order list + ready-to-send WhatsApp order messages."
---

# Santik — Stok Harian & Senarai Oder

Tugas: tukar baki stok yang Encik Minol taip/hantar → status stok + senarai oder ikut supplier + mesej WhatsApp siap hantar. Bahasa: BM santai (rojak OK). Mesra telefon: pendek, jelas, emoji sebagai penanda.

## Input yang diterima
- Senarai taip bebas, cth: `ayam berempah 12, udang 20pcs, sotong 1kg, isi ayam 3kg, susu 2 kotak`
- Nota suara / gambar peti sejuk / gambar kertas stok → baca dan senaraikan semula untuk dia sahkan dulu
- Kalau ada item yang tak jelas (unit/jumlah), tanya SEKALI sahaja, gabung semua soalan dalam satu mesej

## Senarai Par (stok minimum) — isi/kemaskini oleh Encik Minol
Guna senarai ini kalau ada. Kalau item tiada dalam senarai, tanya par level dia sekali, kemudian cadangkan dia tambah ke jadual Par dalam skill ini.

| Item | Unit | Par (minimum) | Oder sampai | Supplier |
|---|---|---|---|---|
| Ayam berempah | pack (1pc/pack) | _isi_ | _isi_ | _isi_ |
| Udang | pcs (3pcs/order) | _isi_ | _isi_ | _isi_ |
| Sotong | g (100g/order) | _isi_ | _isi_ | _isi_ |
| Isi ayam (buttermilk) | g (100g/serving) | _isi_ | _isi_ | _isi_ |

Nota: bahan utama dipek ikut portion. Kalau dia beri jumlah pack, kira juga berapa order boleh dibuat (cth 30 pack udang = 30 order).

## Langkah
1. Sahkan senarai baki (kalau datang dari gambar/suara).
2. Banding dengan Par:
   - 🔴 HABIS / bawah 25% par → wajib oder hari ini
   - 🟡 RENDAH / bawah par → oder
   - 🟢 CUKUP → tak perlu
3. Kira kuantiti oder = (Oder sampai − baki), bundarkan ke unit beli (pack/kg/kotak).
4. Kumpul ikut supplier. Item tanpa supplier → kumpulan "Beli sendiri / pasar".
5. Kalau harga diketahui (dari chat atau rekod resit), tunjuk anggaran kos per supplier + jumlah besar.

## Format output (ikut turutan ini)

**📦 Stok [Hari, Tarikh]**

🔴 Wajib oder: item — baki → oder X
🟡 Rendah: item — baki → oder X
🟢 Cukup: senarai pendek dalam satu baris

**🛒 Oder ikut supplier**
Satu blok per supplier, kemudian mesej WhatsApp siap salin dalam code block:

```
Salam [nama supplier], Santik Kayu Café (Pusat Islam UUM) nak oder untuk [hari/tarikh hantar]:
1. [item] – [kuantiti]
2. ...
Boleh hantar sebelum 9 pagi? Terima kasih 🙏
```

**💰 Anggaran kos:** (jika ada harga)

**✅ Ringkasan:** "X item perlu oder, Y supplier. Siap dalam 2 minit!" + satu baris semangat ringkas.

## Peraturan
- Jangan reka harga atau nama supplier. Kosongkan dan tanya.
- Jangan tambah item yang dia tak sebut.
- Kalau satu item baki = 0 dan ia bahan menu hero (isi ayam buttermilk), letak paling atas dengan ⚠️.
- Bila ada item/par baru, ingatkan: "Tambah par level ni dalam jadual Par di skill (Tetapan > Skills) supaya saya ingat."