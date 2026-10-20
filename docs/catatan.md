## 17 oktober 2026

### Masalah: Pesanan terlupa saat banyak pelanggan datang bersamaan
- **Kondisi:** Pembayaran umumnya dilakukan di akhir. Saat melayani satu pelanggan,
  pelanggan lain datang dan antrian memanjang.
- **Penyebab:** Pesanan hanya diingat, tidak dicatat, sehingga pesanan berikutnya
  sering terlupa.
- **Solusi:** Fitur antrian (open order): pesanan disimpan dengan label dan status
  (Menunggu, Disajikan, Lunas), pembayaran dilakukan setelah pesanan disajikan.
- **Status:** Sudah diterapkan, perlu diuji di warung

## 18 Oktober 2026

### Masalah: Layar HP padam saat menunggu pembeli memilih menu
- **Kondisi:** Saat melayani, kasir menunggu pembeli memilih. Layar HP padam
  otomatis dan kasir harus membuka kunci layar lagi.
- **Penyebab:** Pengaturan layar otomatis mati pada perangkat.
- **Solusi:** Screen Wake Lock API, layar dijaga menyala selama aplikasi dibuka
  dan hanya mati saat tombol power ditekan.
- **Status:** Sudah diterapkan, perlu diuji di HP warung (termasuk saat mode
  hemat baterai aktif)

## 20 Oktober 2026

### Temuan: Pemilik membutuhkan perhitungan keuntungan
- **Kondisi:** Setelah aplikasi ditunjukkan ke pemilik warung, ia menanyakan apakah
  ada kalkulator untuk menghitung keuntungan, karena merasa uang yang didapat
  kurang sesuai perkiraan.
- **Penyebab:** Aplikasi baru mencatat pemasukan, belum mencatat pengeluaran.
- **Solusi:** Fitur pencatatan pengeluaran dan rekap laba harian dan bulanan.
- **Status:** Direncanakan, prioritas lebih tinggi daripada fitur prediksi.

## 21 Oktober 2026

### Masalah: Sulit memeriksa apakah semua pesanan sudah tercatat
- **Kondisi:** Pada pesanan rombongan (12 orang, banyak menu), kasir harus
  membuka halaman detail pesanan untuk memastikan jumlah tiap menu, dan
  sering ada yang tertinggal.
- **Penyebab:** Halaman kasir tidak menampilkan jumlah yang sudah dipesan per menu.
- **Solusi:** Tombol − jumlah + pada tiap menu di halaman kasir, plus total
  porsi per kategori pada tab.
- **Status:** Sudah diterapkan, perlu diuji di warung.

### Masalah: Salah pencet tombol saat terburu-buru
- **Kondisi:** Tombol Simpan ke antrian, Batal, dan Bayar berdekatan sehingga
  sesekali tertekan keliru.
- **Penyebab:** Tombol yang bisa membuang pesanan diletakkan sejajar tombol utama.
- **Solusi:** Batal dipindah ke pojok atas panel dan perlu dua kali ketukan
  untuk konfirmasi. Tombol di sebelah Bayar diganti menjadi Tutup.
- **Status:** Sudah diterapkan, perlu diuji di warung.

### Masalah: Input item bebas terlalu lambat
- **Kondisi:** Untuk menambah item di luar menu, kasir mengetik nominal lengkap
  (misalnya 6000), lebih lambat daripada memakai kalkulator.
- **Penyebab:** Harga harus diketik penuh sampai satuan rupiah.
- **Solusi:** Harga diketik dalam ribuan (6 menjadi Rp 6.000), dengan pratinjau
  harga dan tombol Enter untuk menambah.
- **Status:** Sudah diterapkan, perlu diuji di warung.