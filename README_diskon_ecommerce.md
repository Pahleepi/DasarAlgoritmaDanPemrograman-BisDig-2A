Sistem Kalkulator Diskon E-Commerce
Repository ini berisi implementasi program Python yang menghitung total pembayaran pada sistem e-commerce dengan penerapan diskon berdasarkan jumlah belanja. Program ini dibuat sebagai bagian dari mata kuliah Dasar Algoritma dan Pemrograman untuk program studi Bisnis Digital.

Penjelasan Struktur Kontrol Percabangan untuk Logika Diskon
Konsep Dasar Struktur Kontrol Percabangan
Struktur kontrol percabangan adalah mekanisme pengambilan keputusan dalam pemrograman yang memungkinkan program untuk mengeksekusi blok kode tertentu berdasarkan hasil evaluasi suatu kondisi. Percabangan memungkinkan program untuk "berpikir" dan memutuskan alur eksekusi yang berbeda berdasarkan kondisi yang diberikan.

Implementasi dalam Sistem Diskon E-Commerce
Dalam studi kasus sistem e-commerce ini, struktur kontrol percabangan digunakan untuk menentukan apakah pelanggan berhak mendapatkan diskon berdasarkan total nilai belanja mereka. Logikanya adalah sebagai berikut:

python
if total_belanja > 500000:
    # Jika total belanja lebih dari Rp500.000, berikan diskon 10%
    diskon = total_belanja * 0.1
else:
    # Jika total belanja kurang dari atau sama dengan Rp500.000, tidak ada diskon
    diskon = 0
Struktur percabangan ini memiliki komponen-komponen berikut:

Kondisi: total_belanja > 500000 adalah ekspresi boolean yang dievaluasi oleh program. Jika hasilnya True (total belanja lebih dari Rp500.000), maka blok kode pertama dijalankan. Jika False, blok kode setelah else yang dijalankan.
Blok if: Kode yang dijalankan ketika kondisi bernilai True. Dalam kasus ini, diskon dihitung sebesar 10% dari total belanja.
Blok else: Kode yang dijalankan ketika kondisi bernilai False. Dalam kasus ini, tidak ada diskon yang diberikan (diskon = 0).
Keuntungan Penggunaan Struktur Kontrol Percabangan
Fleksibilitas: Mudah untuk mengubah logika bisnis, seperti mengubah persentase diskon atau batas minimal belanja.
Keterbacaan: Kode menjadi lebih terstruktur dan mudah dipahami, karena jelas kapan diskon diberikan dan kapan tidak.
Ekstensibilitas: Mudah untuk menambahkan kondisi tambahan, misalnya jika ingin menerapkan tingkatan diskon berbeda untuk rentang nilai belanja yang berbeda.
Efisiensi: Program hanya menjalankan blok kode yang relevan dengan kondisi, menghemat sumber daya komputasi.
Variasi Struktur Percabangan dalam Sistem Diskon
Struktur percabangan dapat diperluas untuk menangani berbagai skenario diskon yang lebih kompleks, misalnya:

python
if total_belanja > 1000000:
    # Diskon 15% untuk belanja di atas Rp1.000.000
    diskon = total_belanja * 0.15
elif total_belanja > 500000:
    # Diskon 10% untuk belanja di atas Rp500.000
    diskon = total_belanja * 0.1
else:
    # Tidak ada diskon untuk belanja Rp500.000 ke bawah
    diskon = 0
Struktur ini memungkinkan implementasi kebijakan diskon bertingkat, yang umum digunakan dalam strategi pemasaran e-commerce.

Alur Kerja Program Kalkulator Diskon
Program meminta input total belanja dari pengguna.
Input divalidasi untuk memastikan nilai numerik positif.
Program menentukan apakah total belanja memenuhi syarat untuk mendapatkan diskon (> Rp500.000).
Jika syarat terpenuhi, program menghitung diskon sebesar 10% dari total belanja.
Program menghitung total yang harus dibayar (total belanja - diskon).
Program menampilkan rincian pembayaran: total belanja, diskon, dan total bayar.
Contoh Penggunaan Program
Skenario 1: Total Belanja di Bawah Batas Diskon
PROGRAM KALKULATOR DISKON E-COMMERCE
====================================
Masukkan total belanja (Rp): 400000
Belanja di atas Rp500.000 untuk mendapatkan diskon 10%.

===== RINCIAN PEMBAYARAN =====
Total Belanja: Rp400.000,00
Diskon: Rp0,00
Total Bayar: Rp400.000,00
Skenario 2: Total Belanja di Atas Batas Diskon
PROGRAM KALKULATOR DISKON E-COMMERCE
====================================
Masukkan total belanja (Rp): 750000
Selamat! Anda mendapatkan diskon 10%.

===== RINCIAN PEMBAYARAN =====
Total Belanja: Rp750.000,00
Diskon: Rp75.000,00
Total Bayar: Rp675.000,00
Cara Menjalankan Program
Pastikan Python sudah terinstal di komputer Anda
Unduh file kalkulator_diskon.py
Buka terminal atau command prompt
Navigasikan ke direktori tempat file tersebut berada
Jalankan perintah: python kalkulator_diskon.py
Ikuti instruksi yang muncul untuk memasukkan total belanja
Penerapan di Dunia Bisnis Digital
Sistem diskon otomatis seperti ini sangat umum digunakan dalam platform e-commerce dan merupakan bagian dari strategi pemasaran untuk:

Meningkatkan Nilai Order Rata-Rata: Mendorong pelanggan untuk menambah belanjaan mereka agar mencapai batas diskon.
Meningkatkan Konversi: Mengurangi tingkat abandonment cart saat pelanggan mengetahui adanya peluang mendapatkan diskon.
Segmentasi Pelanggan: Memungkinkan perusahaan untuk memberikan penawaran berbeda kepada segmen pelanggan yang berbeda.
Analisis Data: Memungkinkan bisnis untuk menganalisis efektivitas kebijakan diskon terhadap perilaku pembelian pelanggan.
Pemahaman struktur kontrol percabangan dalam konteks ini adalah dasar penting untuk mengembangkan algoritma bisnis yang lebih kompleks seperti sistem rekomendasi produk, personalisasi penawaran, atau program loyalitas.
