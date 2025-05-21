# 1. Tugas UTS Mata Kuliah Dasar Algoritma dan Pemrograman Bisnis Digital-2A
Dalam file README.md ini menjelaskan konsep, cara kegunaan, dan manfaat dari program yang sudah dibuat berdasarkan soal UTS yang sudah diberikan di web e-campus.

# Faktorial Rekursif

## Apa Itu Faktorial?

Faktorial dari sebuah bilangan bulat positif n, dinotasikan sebagai n!, adalah hasil perkalian dari semua bilangan bulat positif yang kurang dari atau sama dengan n.

Definisi matematika:
- 0! = 1 (definisi khusus)
- 1! = 1
- n! = n × (n-1) × (n-2) × ... × 2 × 1

Contoh:
- 5! = 5 × 4 × 3 × 2 × 1 = 120

## Manfaat Penggunaan Fungsi

1. **Modularitas**: Fungsi memungkinkan kita memecah program kompleks menjadi blok-blok kode yang lebih kecil dan terkelola. Dalam program faktorial ini, kita memisahkan logika perhitungan dari interaksi pengguna.

2. **Reusabilitas**: Fungsi `faktorial()` dapat dipanggil berulang kali tanpa perlu menulis ulang kode yang sama. Fungsi ini bisa digunakan kembali dalam program lain yang membutuhkan perhitungan faktorial.

3. **Abstraksi**: Fungsi menyembunyikan detail implementasi, membuat kode lebih bersih. Pengguna fungsi hanya perlu tahu bahwa fungsi tersebut menghitung faktorial tanpa perlu memahami detailnya.

4. **Pemeliharaan Kode**: Jika ada perubahan pada algoritma faktorial, kita hanya perlu mengubah satu tempat, yaitu fungsi itu sendiri, tidak perlu mengubah seluruh kode.

5. **Keterbacaan**: Kode menjadi lebih terstruktur dan mudah dibaca karena terbagi dalam bagian-bagian logis dengan penamaan yang jelas.

## Apa Itu Rekursi?

Rekursi adalah teknik dalam pemrograman di mana sebuah fungsi memanggil dirinya sendiri untuk menyelesaikan suatu masalah.

## Cara Kerja Rekursi dalam Menghitung Faktorial

Rekursi adalah teknik pemrograman di mana fungsi memanggil dirinya sendiri. Dalam kasus faktorial, rekursi bekerja dengan prinsip:

```
faktorial(n) = n * faktorial(n-1)
```

Dengan kasus dasar:
```
faktorial(0) = 1
faktorial(1) = 1
```

### Contoh Eksekusi Faktorial(5):

1. **faktorial(5)**
   - 5 bukan 0 atau 1, jadi gunakan rumus rekursif
   - Mengembalikan 5 * faktorial(4)
   - Tetapi kita perlu menghitung faktorial(4) dulu
   
2. **faktorial(4)**
   - 4 bukan 0 atau 1, jadi gunakan rumus rekursif
   - Mengembalikan 4 * faktorial(3)
   - Tetapi kita perlu menghitung faktorial(3) dulu
   
3. **faktorial(3)**
   - 3 bukan 0 atau 1, jadi gunakan rumus rekursif
   - Mengembalikan 3 * faktorial(2)
   - Tetapi kita perlu menghitung faktorial(2) dulu
   
4. **faktorial(2)**
   - 2 bukan 0 atau 1, jadi gunakan rumus rekursif
   - Mengembalikan 2 * faktorial(1)
   - Tetapi kita perlu menghitung faktorial(1) dulu
   
5. **faktorial(1)**
   - 1 adalah kasus dasar
   - Mengembalikan 1
   - Sekarang kita mulai menyelesaikan panggilan fungsi sebelumnya dari bawah ke atas

6. **Penyelesaian**:
   - faktorial(1) = 1
   - faktorial(2) = 2 * 1 = 2
   - faktorial(3) = 3 * 2 = 6
   - faktorial(4) = 4 * 6 = 24
   - faktorial(5) = 5 * 24 = 120

Jadi, faktorial(5) = 120.

## Kelebihan dan Keterbatasan Rekursi

**Kelebihan**:
- Solusi yang elegan dan intuitif untuk masalah yang bersifat rekursif secara alami
- Kode menjadi lebih pendek dan bersih
- Lebih mudah dipahami untuk algoritma tertentu

**Keterbatasan**:
- Memakan lebih banyak memori karena setiap panggilan rekursif menyimpan informasi di call stack
- Risiko stack overflow untuk input yang besar
- Terkadang kurang efisien dibandingkan pendekatan iteratif

## Contoh Output Program

```
Masukkan angka untuk dihitung faktorialnya: 5
Faktorial dari 5 adalah 120
```

## Kapan Rekursi Digunakan?

1. **Masalah yang dapat dibagi menjadi submasalah yang identik**
   - Perhitungan faktorial
   - Fibonacci
   - Pencarian biner
   - Algoritma divide-and-conquer

2. **Struktur data rekursif**
   - Pohon (traversal, pencarian)
   - Graf (DFS, BFS)
   - Linked list

3. **Kasus di mana solusi rekursif lebih jelas dan mudah dipahami**
   - Algoritma backtracking (seperti 8-queen problem)
   - Algoritma dalam permainan (seperti catur)

4. **Definisi matematis yang secara alami rekursif**
   - Pengurutan (merge sort, quicksort)
   - Tower of Hanoi
   - Problem kombinatorial

## Kapan Rekursi Tidak Cocok Digunakan

1. **Kedalaman rekursi yang besar**
Risiko stack overflow
Contoh: Menghitung Fibonacci untuk angka besar

2. **Masalah yang lebih efisien diselesaikan secara iteratif**
Loop sederhana lebih cepat daripada pemanggilan fungsi berulang
Contoh: Perulangan array sederhana

3. **Keterbatasan memori**
Setiap pemanggilan rekursif menggunakan memori di stack
Tidak cocok untuk perangkat dengan memori terbatas

4. **Ketika performa menjadi perhatian utama**
Rekursi biasanya lebih lambat karena overhead pemanggilan fungsi
Contoh: Pemrosesan real-time atau aplikasi dengan data besar

5. **Kasus yang membutuhkan kontrol aliran yang kompleks**
Rekursi sulit untuk dihentikan di tengah proses
Penanganan kesalahan lebih rumit dalam fungsi rekursif

## Catatan Pembelajaran

Fungsi rekursif faktorial ini merupakan contoh sederhana namun kuat untuk memahami konsep rekursi dalam pemrograman. Konsep ini menjadi dasar untuk memahami algoritma-algoritma yang lebih kompleks seperti traversal tree, backtracking, dan dynamic programming.

Dalam konteks bisnis digital, pemahaman fungsi rekursif membantu dalam pengembangan algoritma untuk:
- Analisis struktur data kompleks
- Pengolahan data hierarkis
- Optimisasi proses bisnis
- Pengembangan sistem cerdas

# 2. Pencarian Nilai Tertinggi Siswa Menggunakan Perulangan dan Array

## Penjelasan Penggunaan Perulangan dan Array dalam Kasus Ini

### 1. Penggunaan Array (List)

Array dalam Python diimplementasikan sebagai struktur data list. Dalam studi kasus ini, list digunakan untuk:

- **Penyimpanan Data**: Menyimpan nilai-nilai dari 5 siswa dalam satu struktur data yang mudah diakses.
- **Indexing**: Memungkinkan akses ke nilai spesifik melalui posisi indeksnya.
- **Operasi Kolektif**: Memungkinkan operasi seperti pencarian nilai maksimum (`max()`) pada seluruh kumpulan data dengan mudah.

List dalam program ini (`nilai_siswa`) berfungsi sebagai wadah yang menyimpan nilai numerik setiap siswa secara berurutan. Indeks dalam list (dimulai dari 0) dapat digunakan untuk mengidentifikasi siswa ke berapa yang memiliki nilai tertentu.

## Manfaat Array 

- Penyimpanan Efisien: Menyimpan banyak data dengan nama variabel yang sama
- Akses Cepat: Mengakses elemen dengan kompleksitas waktu konstan
- Pengelolaan Data: Mempermudah manipulasi sekelompok data terkait
- Optimasi Memori: Menghemat memori dengan struktur homogen
- Dasar Algoritma: Fundamental untuk banyak algoritma penting

### 2. Penggunaan Perulangan

Dalam studi kasus ini, perulangan digunakan untuk:

1. **Perulangan `for` untuk Input**: Mengotomatisasi proses pengumpulan nilai dari 5 siswa tanpa perlu menulis kode input yang berulang.
   ```python
   for i in range(5):
       # kode untuk input nilai siswa ke-i
   ```

2. **Perulangan `while` untuk Validasi**: Memastikan input pengguna valid (numerik dan dalam rentang 0-100) dengan meminta input ulang jika tidak memenuhi kriteria.
   ```python
   while True:
       # mencoba mendapatkan input yang valid
       # keluar dari loop jika valid
   ```

3. **List Comprehension** (bentuk perulangan ringkas): Digunakan untuk menemukan semua siswa yang memiliki nilai tertinggi yang sama.
   ```python
   nilai_sama = [i+1 for i, nilai in enumerate(nilai_siswa) if nilai == nilai_tertinggi]
   ```

Perulangan memungkinkan program untuk mengeksekusi tugas berulang seperti pengumpulan input atau pemrosesan data dengan kode yang ringkas dan efisien.

## Manfaat Perulangan 

- Efisiensi Kode: Mengurangi repetisi kode
- Skalabilitas: Memproses data dalam jumlah besar tanpa menulis lebih banyak kode
- Fleksibilitas: Dapat digunakan untuk berbagai skenario pemrosesan data
- Pemeliharaan Kode: Lebih mudah memperbarui dan memperbaiki kode

## Alur Kerja Program

1. Program meminta pengguna memasukkan nilai untuk 5 siswa satu per satu.
2. Setiap nilai divalidasi: harus berupa angka dan berada dalam rentang 0-100.
3. Nilai-nilai disimpan dalam sebuah list.
4. Program mencari nilai tertinggi menggunakan fungsi `max()`.
5. Program menentukan siswa ke berapa yang mendapatkan nilai tertinggi menggunakan indeks.
6. Program menampilkan nilai tertinggi dan siswa yang mendapatkannya.
7. Jika ada beberapa siswa dengan nilai tertinggi yang sama, program akan menampilkan informasi ini.

## Contoh Output Program

```
MENCARI NILAI TERTINGGI SISWA
=============================
Input nilai siswa ke-1: 75
Input nilai siswa ke-2: 82
Input nilai siswa ke-3: 90
Input nilai siswa ke-4: 78
Input nilai siswa ke-5: 88

Nilai semua siswa: [75.0, 82.0, 90.0, 78.0, 88.0]
Nilai tertinggi: 90.0
Diperoleh oleh siswa ke-3
```

## Konsep Penting yang Digunakan

1. **List sebagai Struktur Data**: Penyimpanan dan manipulasi data nilai siswa
2. **Perulangan**: Pengumpulan input dan proses data secara efisien
3. **Pemrosesan Input**: Validasi input untuk memastikan data yang valid
4. **Pencarian Nilai Maksimum**: Menggunakan fungsi bawaan Python (`max()`)
5. **Penanganan Indeks**: Konversi indeks ke nomor siswa (indeks+1)
6. **Penanganan Kasus Khusus**: Deteksi nilai tertinggi yang sama pada beberapa siswa

Konsep-konsep yang digunakan dalam program ini (array, perulangan, pencarian nilai) adalah dasar yang penting dalam pengembangan sistem informasi bisnis, seperti:

- Sistem penilaian kinerja karyawan
- Analisis data penjualan untuk menemukan produk terlaris
- Pengolahan data pelanggan untuk program loyalitas
- Sistem pendukung keputusan untuk identifikasi peluang bisnis

Kemampuan untuk menyimpan, memproses, dan menganalisis data menggunakan struktur data dan algoritma yang tepat adalah keterampilan fundamental dalam pengembangan solusi bisnis digital.

# 3. Kalkulator Diskon E-Commerce Menggunkan Struktur Kontrol Percabangan

## Penjelasan Struktur Kontrol Percabangan untuk Logika Diskon

### Konsep Dasar Struktur Kontrol Percabangan

Struktur kontrol percabangan adalah mekanisme pengambilan keputusan dalam pemrograman yang memungkinkan program untuk mengeksekusi blok kode tertentu berdasarkan hasil evaluasi suatu kondisi. Percabangan memungkinkan program untuk "berpikir" dan memutuskan alur eksekusi yang berbeda berdasarkan kondisi yang diberikan.

### Implementasi dalam Sistem Diskon E-Commerce

Dalam studi kasus sistem e-commerce ini, struktur kontrol percabangan digunakan untuk menentukan apakah pelanggan berhak mendapatkan diskon berdasarkan total nilai belanja mereka. Logikanya adalah sebagai berikut:

```python
if total_belanja > 500000:
    # Jika total belanja lebih dari Rp500.000, berikan diskon 10%
    diskon = total_belanja * 0.1
else:
    # Jika total belanja kurang dari atau sama dengan Rp500.000, tidak ada diskon
    diskon = 0
```

Struktur percabangan ini memiliki komponen-komponen berikut:

1. **Kondisi**: `total_belanja > 500000` adalah ekspresi boolean yang dievaluasi oleh program. Jika hasilnya `True` (total belanja lebih dari Rp500.000), maka blok kode pertama dijalankan. Jika `False`, blok kode setelah `else` yang dijalankan.

2. **Blok if**: Kode yang dijalankan ketika kondisi bernilai `True`. Dalam kasus ini, diskon dihitung sebesar 10% dari total belanja.

3. **Blok else**: Kode yang dijalankan ketika kondisi bernilai `False`. Dalam kasus ini, tidak ada diskon yang diberikan (diskon = 0).

### Keuntungan Penggunaan Struktur Kontrol Percabangan

1. **Fleksibilitas**: Mudah untuk mengubah logika bisnis, seperti mengubah persentase diskon atau batas minimal belanja.

2. **Keterbacaan**: Kode menjadi lebih terstruktur dan mudah dipahami, karena jelas kapan diskon diberikan dan kapan tidak.

3. **Ekstensibilitas**: Mudah untuk menambahkan kondisi tambahan, misalnya jika ingin menerapkan tingkatan diskon berbeda untuk rentang nilai belanja yang berbeda.

4. **Efisiensi**: Program hanya menjalankan blok kode yang relevan dengan kondisi, menghemat sumber daya komputasi.

### Variasi Struktur Percabangan dalam Sistem Diskon

Struktur percabangan dapat diperluas untuk menangani berbagai skenario diskon yang lebih kompleks, misalnya:

```python
if total_belanja > 1000000:
    # Diskon 15% untuk belanja di atas Rp1.000.000
    diskon = total_belanja * 0.15
elif total_belanja > 500000:
    # Diskon 10% untuk belanja di atas Rp500.000
    diskon = total_belanja * 0.1
else:
    # Tidak ada diskon untuk belanja Rp500.000 ke bawah
    diskon = 0
```

Struktur ini memungkinkan implementasi kebijakan diskon bertingkat, yang umum digunakan dalam strategi pemasaran e-commerce.

## Alur Kerja Program Kalkulator Diskon

1. Program meminta input total belanja dari pengguna.
2. Input divalidasi untuk memastikan nilai numerik positif.
3. Program menentukan apakah total belanja memenuhi syarat untuk mendapatkan diskon (> Rp500.000).
4. Jika syarat terpenuhi, program menghitung diskon sebesar 10% dari total belanja.
5. Program menghitung total yang harus dibayar (total belanja - diskon).
6. Program menampilkan rincian pembayaran: total belanja, diskon, dan total bayar.

## Contoh Penggunaan Program

### Skenario 1: Total Belanja di Bawah Batas Diskon

```
PROGRAM KALKULATOR DISKON E-COMMERCE
====================================
Masukkan total belanja (Rp): 400000
Maaf, Anda tidak mendapatkan diskon.

===== RINCIAN PEMBAYARAN =====
Total Belanja: Rp400.000,00
Diskon: Rp0,00
Total Bayar: Rp400.000,00
```

### Skenario 2: Total Belanja di Atas Batas Diskon

```
PROGRAM KALKULATOR DISKON E-COMMERCE
====================================
Masukkan total belanja (Rp): 750000
Selamat! Anda mendapatkan diskon 10%.

===== RINCIAN PEMBAYARAN =====
Total Belanja: Rp750.000,00
Diskon: Rp75.000,00
Total Bayar: Rp675.000,00
```

### Skenario 3: Total Belanja Sama Dengan Batas Diskon

```
PROGRAM KALKULATOR DISKON E-COMMERCE
====================================
Masukkan total belanja (Rp): 500000
Belanja di atas Rp500.000 untuk mendapatkan diskon 10%.

===== RINCIAN PEMBAYARAN =====
Total Belanja: Rp500.000,00
Diskon: Rp0,00
Total Bayar: Rp500.000,00
```

## Cara Menjalankan Program

1. Pastikan Python sudah terinstal di komputer Anda
2. Unduh file `kalkulator_diskon.py`
3. Buka terminal atau command prompt
4. Navigasikan ke direktori tempat file tersebut berada
5. Jalankan perintah: `python kalkulator_diskon.py`
6. Ikuti instruksi yang muncul untuk memasukkan total belanja

## Penerapan di Dunia Bisnis Digital

Sistem diskon otomatis seperti ini sangat umum digunakan dalam platform e-commerce dan merupakan bagian dari strategi pemasaran untuk:

1. **Meningkatkan Nilai Order Rata-Rata**: Mendorong pelanggan untuk menambah belanjaan mereka agar mencapai batas diskon.

2. **Meningkatkan Konversi**: Mengurangi tingkat abandonment cart saat pelanggan mengetahui adanya peluang mendapatkan diskon.

3. **Segmentasi Pelanggan**: Memungkinkan perusahaan untuk memberikan penawaran berbeda kepada segmen pelanggan yang berbeda.

4. **Analisis Data**: Memungkinkan bisnis untuk menganalisis efektivitas kebijakan diskon terhadap perilaku pembelian pelanggan.

Pemahaman struktur kontrol percabangan dalam konteks ini adalah dasar penting untuk mengembangkan algoritma bisnis yang lebih kompleks seperti sistem rekomendasi produk, personalisasi penawaran, atau program loyalitas.

# 4. Program Penentu Kelulusan Berdasarkan Rata-rata Nilai

## Peran Tipe Data dan Operator dalam Perhitungan Rata-rata

### Tipe Data yang Digunakan

Dalam program ini, beberapa tipe data yang berperan penting adalah:

1. **Float**
   - Digunakan untuk menyimpan nilai ujian karena nilai dapat berupa bilangan desimal.
   - Contoh: `nilai_matematika = 85.5`
   - Float memungkinkan perhitungan yang lebih presisi dibandingkan integer, terutama untuk pembagian dan rata-rata.

2. **Integer**
   - Digunakan untuk menyimpan jumlah mata pelajaran (`jumlah_mapel = 3`).
   - Merepresentasikan bilangan bulat tanpa komponen desimal.

3. **Boolean**
   - Menyimpan hasil evaluasi kondisi kelulusan (`is_lulus = rata_rata >= 75`).
   - Hanya memiliki dua nilai: `True` atau `False`.
   - Sangat penting untuk logika percabangan.

4. **String**
   - Digunakan untuk menyimpan status kelulusan ("LULUS" atau "TIDAK LULUS").
   - Memungkinkan kita menyajikan hasil dalam format yang mudah dibaca manusia.

### Operator yang Digunakan

Program ini mendemonstrasikan penggunaan berbagai jenis operator:

1. **Operator Aritmatika**
   - Penjumlahan (`+`): Menghitung total nilai semua mata pelajaran.
     ```python
     jumlah_nilai = nilai_matematika + nilai_bahasa + nilai_ipa
     ```
   - Pembagian (`/`): Menghitung rata-rata dengan membagi jumlah nilai dengan jumlah mata pelajaran.
     ```python
     rata_rata = jumlah_nilai / jumlah_mapel
     ```
   - Pengurangan (`-`): Menghitung poin yang dibutuhkan untuk lulus.
     ```python
     poin_kurang = 75 - rata_rata
     ```

2. **Operator Perbandingan**
   - Lebih besar atau sama dengan (`>=`): Membandingkan rata-rata dengan nilai minimum untuk lulus.
     ```python
     is_lulus = rata_rata >= 75
     ```
   - Operator perbandingan lain seperti `<=`, `==`, dan `!=` juga penting dalam validasi range nilai.
     ```python
     if not (0 <= nilai <= 100):  # Menggunakan <= dua kali
     ```

3. **Operator Logika**
   - `not`: Membalikkan nilai boolean, digunakan untuk kondisi tidak lulus.
     ```python
     if not is_lulus:
     ```

4. **Operator Ternary (Conditional Expression)**
   - Digunakan untuk menetapkan nilai berdasarkan kondisi dalam satu baris.
     ```python
     status = "LULUS" if is_lulus else "TIDAK LULUS"
     ```

### Bagaimana Tipe Data dan Operator Bekerja Bersama

1. **Konversi Tipe Data**
   - Input dari pengguna awalnya berupa string dan harus dikonversi ke float:
     ```python
     nilai_matematika = float(input("Masukkan nilai Matematika: "))
     ```
   - Konversi ini memastikan bahwa nilai dapat digunakan dalam operasi matematis.

2. **Alur Perhitungan**
   - Nilai diinput sebagai float
   - Dihitung jumlah dengan operator penjumlahan
   - Dihitung rata-rata dengan operator pembagian
   - Hasil rata-rata (float) dibandingkan dengan kriteria kelulusan menggunakan operator perbandingan
   - Hasil perbandingan (boolean) digunakan untuk menentukan status (string)

3. **Presisi Numerik**
   - Format output menggunakan `:.2f` untuk membatasi jumlah digit desimal, meningkatkan keterbacaan.
     ```python
     print(f"Rata-rata nilai: {rata_rata:.2f}")
     ```

## Alur Kerja Program

1. Pengguna diminta untuk memasukkan nilai untuk 3 mata pelajaran (Matematika, Bahasa, dan IPA).
2. Program memvalidasi setiap nilai untuk memastikan berada dalam rentang yang valid (0-100).
3. Program menghitung jumlah nilai dan membaginya dengan jumlah mata pelajaran untuk mendapatkan rata-rata.
4. Program mengevaluasi apakah rata-rata memenuhi syarat kelulusan (≥ 75).
5. Program menampilkan semua nilai, rata-rata, dan status kelulusan.
6. Jika siswa tidak lulus, program juga menampilkan berapa poin tambahan yang dibutuhkan untuk mencapai kelulusan.

## Contoh Penggunaan Program

### Skenario 1: Siswa Lulus

```
PROGRAM PENENTU KELULUSAN BERDASARKAN RATA-RATA NILAI
====================================================
Masukkan nilai Matematika: 80
Masukkan nilai Bahasa: 75
Masukkan nilai IPA: 85

===== HASIL PERHITUNGAN =====
Nilai Matematika: 80.0
Nilai Bahasa: 75.0
Nilai IPA: 85.0
Rata-rata nilai: 80.00
Status kelulusan: LULUS
```

### Skenario 2: Siswa Tidak Lulus

```
PROGRAM PENENTU KELULUSAN BERDASARKAN RATA-RATA NILAI
====================================================
Masukkan nilai Matematika: 65
Masukkan nilai Bahasa: 70
Nilai IPA: 75

===== HASIL PERHITUNGAN =====
Nilai Matematika: 65.0
Nilai Bahasa: 70.0
Nilai IPA: 75.0
Rata-rata nilai: 70.00
Status kelulusan: TIDAK LULUS
Anda memerlukan 5.00 poin lagi untuk lulus.
```

## Penerapan Konsep dalam Bisnis Digital

Konsep tipe data dan operator yang dibahas merupakan fondasi penting dalam pengembangan aplikasi bisnis digital, seperti:

1. **Sistem Penilaian Kinerja**: Menghitung rata-rata KPI karyawan dan menentukan kelayakan bonus atau promosi.

2. **Analisis Finansial**: Mengolah data keuangan, menghitung rasio-rasio penting, dan membuat keputusan berdasarkan threshold tertentu.

3. **Sistem Rekomendasi**: Menghitung skor relevansi produk berdasarkan beberapa parameter dan menampilkan rekomendasi jika skor di atas ambang batas tertentu.

4. **Dashboard Analytics**: Mengolah dan menampilkan data bisnis, sering kali membutuhkan perhitungan rata-rata dan perbandingan dengan target.

Memahami tipe data dan operator dengan baik merupakan keterampilan fundamental yang diperlukan untuk mengembangkan solusi teknologi yang handal dalam bisnis digital.

#5. Program Penghitung Harga Barang

Program sederhana untuk menghitung total harga dari 3 barang yang diinput oleh pengguna.

## Deskripsi

Program ini dibuat untuk membantu penghitungan total harga dari 3 barang. Program akan menerima input harga dari pengguna dan menampilkan rincian serta total harga pembelian.

## Fitur

- Input harga untuk 3 barang
- Validasi input (hanya menerima angka)
- Menghitung total harga
- Menampilkan rincian pembelian dengan format mata uang Rupiah (Rp)

## Cara Penggunaan

1. Jalankan program dengan perintah:
   ```
   python menghitung_harga_barang.py
   ```

2. Masukkan harga untuk ketiga barang saat diminta:
   ```
   Masukkan harga 3 barang:
   Harga barang ke-1: Rp [masukkan harga]
   Harga barang ke-2: Rp [masukkan harga]
   Harga barang ke-3: Rp [masukkan harga]
   ```

3. Program akan menampilkan rincian pembelian dan total harga:
   ```
   ==== RINCIAN PEMBELIAN ====
   Harga barang 1: Rp x,xxx.xx
   Harga barang 2: Rp x,xxx.xx
   Harga barang 3: Rp x,xxx.xx
   --------------------------

   Total Harga adalah: Rpx,xxx.xx
   ==========================
   Terima kasih telah berbelanja!
   ```

## Catatan

- Input harus berupa angka. Jika bukan angka, program akan menampilkan pesan kesalahan: "Input harus berupa angka!"
- Program menggunakan format mata uang Indonesia (Rupiah) dengan pemisah ribuan dan 2 angka desimal

## Pengembangan

Program ini dapat dikembangkan lebih lanjut dengan menambahkan fitur-fitur seperti:
- Perhitungan diskon
- Input jumlah barang yang fleksibel
- Penyimpanan data pembelian
- Interface grafis
