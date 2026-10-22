NAMA : BINTANG ZAHRA MEIZIQRA
NIM : 2311060058
INFORMATIKA 6

# simulasi-monte-carlo-kereta-api
**LAPORAN PROYEK SIMULASI DAN PEMODELAN**
Simulasi Ketidakpastian Jumlah Penumpang Kereta Api Jabodetabek Menggunakan Metode Monte Carlo berdasarkan data BPS tahun 2023-2026

**I.	Deksripsi Projek**
  Di wilayah jabodetabek, kereta api adalah salah satu sarana transportasi publik yang menjadi andalan utama masyarakat untuk bermobilitas harian. Jumlah penumpang kereta api di Jabodetabek memiliki perubahan setiap bulannya. Hingga perubahan untuk periode selanjutnya tidak bisa di prediksi secara pasti. Di kondisi inilah menjadi dasar pemilihan studi kasus dalam proyek simulasi dan pemodelan.
  Dengan mengambil basis data yang mengeksplorasi data historis penumpang kereta Jabodetabek rilisan Badan Pusat Statistik (BPS) dari Januari 2023 hingga Agustus 2026. Data tersebut digunakan untuk melihat pola perubahan penumpang dan menjadi dasar dalam membuat simulasi penelitian menggunakan metode Monte Carlo.
  Tujuan dalam simulasi ini sebagai perkiraan kemungkinan jumlah penumpang dan membandingkan hasil dengan data aktual, sehingga hasil yang diharapkan bisa menggambarkan ketidakpastian jumlah penumpang berdasarkan catatan periode sebelumnya.

**II.	Sumber Data**
  Dataset yang diekstrak dari table Jumlah Penumpang Kereta Api di laman resmi BPS (Tabel Dinamis - Badan Pusat Statistik Indonesia, https://www.bps.go.id/id/statistics-table/2/NzIjMg%3D%3D/jumlah-penumpang-kereta-api) ini mencakup periode pengamatan Januari 2023 sampai Agustus 2026. Untuk pemrosesan awal, data diunduh dalam ekstensi CSV dengan satuan Kuantitas per ribu orang.
Dalam proyek ini data dibatasi dalam kategori wilayah Jabodetabek agar penumpang yang di analisis tetap konsisten.

**III.	Metode Simulasi dan Pemodelan**
Tahapan simulasi dilakukan beberapa tahap :
1.	Mengolah data jumlah penumpang tahun 2023-2026 dari BPS.
2.	Menghitung pola perubahan dari data historis setiap periode.
3.	Mengambil sampel perubahan historis secara acak dengan pengulangan.
4.	Melakukan 1.000 percobaan simulasi Monte Carlo.
5.	Menghitung rata-rata hasil simulasi dan interval.
6.	Hasil simulasi akan dilakukan perbandingan dengan data penumpang secara data aktual BPS.

**IV.	Hasil Simulasi**
| Indikator | Validasi 2025 | Pengujian 2026 |
|---|---:|---:|
| MAE (ribu orang) | 1390.21 | 1026.91 |
| WAPE (%) | 4.78 | 3.41 |
| Cakupan interval 80% (%) | 41.67 | 75.00 |
Hasil pengujian tahun 2026 menunjukkan WAPE sebesar 3.41%. Artinya, total kesalahan absolut perkiraan setara dengan 3.41% dari jumlah penumpang aktual secara periode pengujian.

**V.	Kesimpulan**
Dari hasil simulasi Monte Carlo menggunakan data BPS 2023 – 2026 menunjukkan bahwa jumlah penumpang kereta api Jabodetabek mengalami perubahan setiap bulan. Berdasarkan pengujian Januari – Agustus 2026, diperoleh WAPE sebesar 3.41%. Hasil tersebut menunjukkan bahwa Metode Monte Carlo dapat digunakan untuk menggambarkan ketidakpastian jumlah penumpang, meskipun hasil perkiraannya masih memiliki selisih dengan data aktual.  

## Cara Menjalankan
1. Buka file notebook .ipynb di Google Colab.
2. Jalankan cell dari awal secara berurutan.
3. Upload file CSV BPS ketika diminta.
4. Jalankan proses simulasi dan evaluasi.
5. Lihat hasil tabel dan grafik.

## Bahasa Pemrograman
- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib

## Dokumentasi Penggunaan AI
Tools AI: ChatGPT
Bentuk bantuan: Diskusi pemilihan studi kasus, penyusunan dokumentasi, serta bantuan pembuatan dan perbaikan kode Python.
Hasil pemeriksaan GPTZero: AI Probability 1% (Human Generated).
Bukti pendukung: Laporan pemeriksaan file GPTZero Ai Scan
