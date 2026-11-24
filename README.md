# Laporan Keuangan Rumah

Dashboard satu halaman untuk memantau uang masuk dan keluar di rumah. Datanya dicatat di Google Sheets, dan halaman ini membacanya lalu menampilkan ringkasan dan grafik.

**Buka:** [zynxx24.github.io/Laporan-Keuangan-Home](https://zynxx24.github.io/Laporan-Keuangan-Home/)

## Isi dashboard

- Total pemasukan, total pengeluaran, net income, jumlah transaksi, dan indeks keuangan.
- Detail transaksi yang bisa diurutkan berdasarkan tanggal.
- Analisis per kuartal.
- Monthly Chain Flow: perpindahan uang dari bulan ke bulan.
- Rincian dan statistik per kategori.

## Cara kerja

Halaman mengunduh Google Sheets yang dipublikasikan sebagai `.xlsx`, membacanya di browser dengan [SheetJS](https://sheetjs.com), lalu menggambar grafik dengan [Chart.js](https://www.chartjs.org). Tidak ada server sama sekali.

Sheet yang dibaca:

| Sheet | Isi |
|---|---|
| `LOG_PENGELUARAN` | Catatan setiap transaksi |
| `CHAIN_MONTH` | Ringkasan per bulan |
| `FINAL` | Angka akhir untuk kartu ringkasan |

Untuk memakai sheet sendiri: buat Google Sheets dengan tiga sheet di atas, pilih File > Bagikan > Publikasikan ke web dengan format Microsoft Excel (.xlsx), lalu ganti nilai `FilePath` di `index.html` dengan link tersebut.

## Jalankan di komputer sendiri

Tidak perlu build. Buka `index.html` di browser (butuh internet untuk mengambil sheet dan library dari CDN).

Lisensi [MIT](LICENSE).
