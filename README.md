# 🍜 POS Warung PWA

Sistem Point of Sale (kasir) berbasis Progressive Web App untuk warung makan, dengan fitur prediksi kebutuhan porsi harian. Dikembangkan sebagai bagian dari tugas akhir/skripsi.

> **Status:** 🚧 Dalam pengembangan (Tahap 1: kalkulator pesanan)

<!-- Ganti dengan screenshot atau GIF demo setelah aplikasi jalan -->
![Screenshot aplikasi](docs/screenshot.png)

**Demo:** [isi link deploy di sini]

---

## Latar Belakang

Pada jam ramai, penghitungan total pesanan di warung masih memakai kalkulator HP. Akibatnya ada menu yang terlewat atau terhitung dobel, dan proses pembayaran jadi lambat. Selain itu, jumlah porsi yang disiapkan tiap hari masih berdasarkan perkiraan, sehingga bisa kelebihan (sisa) atau kekurangan (menu habis).

Proyek ini bertujuan:
1. Mempercepat dan mengurangi kesalahan penghitungan pesanan.
2. Tetap bisa dipakai saat internet putus (offline-first).
3. Memprediksi kebutuhan porsi hari berikutnya dari data penjualan.

## Fitur

**Sudah ada**
- [x] Daftar menu dengan kategori (Makanan, Minuman, Tambahan)
- [x] Keranjang pesanan dengan tombol tambah/kurang
- [x] Total otomatis, uang dibayar (tombol cepat bisa dijumlahkan), dan kembalian
- [x] Item bebas (harga diketik manual)

**Rencana**
- [ ] Penyimpanan transaksi di perangkat (IndexedDB)
- [ ] Riwayat transaksi dan halaman admin menu
- [ ] PWA: bisa di-install dan jalan offline
- [ ] Sinkronisasi ke cloud (Supabase)
- [ ] Laporan penjualan harian dan bulanan
- [ ] Pencatatan menu habis (sold out)
- [ ] Prediksi kebutuhan porsi per menu

## Teknologi

| Bagian | Teknologi |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Penyimpanan lokal | IndexedDB |
| PWA | Web App Manifest, Service Worker |
| Backend/Database | Supabase *(rencana)* |
| Prediksi | Python: pandas, statsmodels, scikit-learn *(rencana)* |

## Cara Menjalankan

```bash
# 1. Clone repo
git clone https://github.com/<username>/pos-warung-pwa.git
cd pos-warung-pwa

# 2. Jalankan server lokal (pilih salah satu)
npx serve .
# atau
python -m http.server 8000
```

Buka `http://localhost:3000` (atau `:8000`) di browser. Untuk mencoba fitur PWA di HP, akses lewat HTTPS (misalnya hasil deploy Netlify/Vercel/GitHub Pages).

## Cara Mengubah Menu

Edit array `menu` di bagian atas script:

```js
{ id: 1, kategori: "Makanan", nama: "Nasi Goreng", harga: 15000 },
```

Setiap menu butuh `id` yang unik. Tombol uang cepat diatur lewat array `pecahan`.

## Struktur Proyek

```
pos-warung-pwa/
├── index.html        # Halaman utama (sementara satu file)
├── docs/             # Screenshot, catatan desain, diagram
└── README.md
```
<!-- Perbarui struktur ini saat file mulai dipisah (css/, js/, sw.js, manifest.json) -->

## Metode Prediksi *(rencana)*

Perbandingan beberapa metode untuk memprediksi permintaan per menu per hari:
- Moving Average (baseline)
- Holt-Winters (exponential smoothing)
- SARIMA
- Random Forest / XGBoost

Evaluasi menggunakan MAE, RMSE, dan MAPE.

## Roadmap

- [x] **Tahap 1:** Kalkulator pesanan
- [ ] **Tahap 2:** Simpan transaksi (IndexedDB)
- [ ] **Tahap 3:** Jadi PWA dan deploy
- [ ] **Tahap 4:** Uji coba di warung
- [ ] **Tahap 5:** Sinkronisasi cloud
- [ ] **Tahap 6:** Laporan dan prediksi

## Catatan Pengembangan

<!-- Catatan masalah yang ditemukan saat uji coba di warung dan keputusan desainnya bisa ditulis di `docs/catatan.md`. -->

## Penulis

**[Muhammad Abdurrohman]**
Mahasiswa Teknik Informatika, Universitas Nusantara PGRI Kediri.
GitHub: [@amdma](https://github.com/amdma)

## Lisensi


