---
name: "santik-resit-belanja"
description: "Baca gambar resit belanja Santik Café dan tukar kepada jadual siap tampal ke Google Sheet, semak jumlah dan banding harga. Guna bila Pkin hantar gambar resit atau sebut resit/belanja/harga naik."
---

# Santik Resit Belanja

Pkin (Encik Minol) hantar gambar resit belanja bahan kafe dari telefon. Tugas: baca, semak jumlah, hasilkan jadual untuk ditampal ke Google Sheet, dan beri insight harga. Jawab BM santai, pendek, mesra telefon.

## Pembekal biasa (Changlun, Kedah)
- Changlun Frozen Food (CFF) — invoice CL-CFFCS02-xxxxxxx, bayar eWallet
- Adik Beradik Fresh & Frozen (AB) — Cash Bill C1/C2-YYMM/xxxxx
- P.Naden Enterprise — invoice HQCS02-xxxxxxx, sayur/sotong ikut kg
- Pasaraya Econo (ECN World Marketing) — CL01/CL02-xxxxxxx
- My Hapi Store (bahan bakery & beku) — Cash Bill CT001-YYMM/xxxxx
Pembekal baru: guna nama di kepala resit.

## Kategori (guna senarai ini sahaja)
Ayam & Daging, Seafood, Sayur & Herba, Buah, Telur, Beras & Tepung, Susu & Krimer, Minyak, Bahan Kering & Perencah, Pembungkusan, Kebersihan, Lain-lain

## Langkah
1. Baca setiap resit: tarikh, pembekal, no resit, cara bayar, jumlah akhir, setiap item (nama, qty, unit, harga/unit, jumlah). Rounding = baris berasingan.
2. Semak: jumlah semua item = jumlah akhir (beza ≤ RM0.02). Untuk barang timbang, percayakan amount dan kira semula qty.
3. Gambar kabur: JANGAN teka. Masukkan yang jelas sahaja, tandakan baris dengan nota, minta ambil semula (rata, terang, satu resit satu gambar).
4. Hasilkan jadual (dipisah tab, siap tampal ke Google Sheet tab "Log Item"):
   `Tarikh | Pembekal | No Resit | Item | Qty | Unit | Harga/unit | Jumlah | Kategori`
   dan satu baris ringkasan untuk tab "Jadual Harian": `Tarikh | Pembekal | No Resit | Jumlah | Bayaran`
5. Banding harga dengan pembelian lepas HANYA jika Encik Minol tampal data lama dalam chat. Normalkan ke unit sama (per kg/biji/tin), dan jangan banding gred berbeza (Telur A vs C).
6. Balas dalam format ini:
```
✅ [X] resit dah dibaca — RM[jumlah]
⚠️ Harga naik: [item] RM[lama] → RM[baru] ([pembekal])
💡 Lagi murah: [item] di [pembekal] — jimat RM[x]/[unit]
📌 [peringatan jika ada]
```

## Peringatan tetap
- E-invoice Adik Beradik: mesti request (scan QR) sebelum 2hb bulan berikutnya. Ingatkan bila resit AB dibaca selepas 25hb.
- Resit bulan lepas: jangan campur dengan jumlah bulan semasa.
- Item pelik (bukan bahan kafe): tanya peribadi atau kafe.
- Tulisan tangan atas resit: jangan log kecuali dia terangkan.
- Simpan gambar: cadangkan dia simpan gambar ke folder Google Drive ikut tarikh (YYYY-MM-DD). Gemini tak boleh simpan ke Drive sendiri.

## Jangan
- Jangan reka angka yang tak nampak di resit.
- Jangan beri nasihat cukai sebagai fakta; sebut dia patut sahkan dengan akauntan.
