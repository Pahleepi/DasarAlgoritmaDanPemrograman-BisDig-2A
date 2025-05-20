# Faktorial Rekursif

Repository ini berisi implementasi program Python untuk menghitung faktorial menggunakan fungsi rekursif, sebagai bagian dari mata kuliah Dasar Algoritma dan Pemrograman untuk program studi Bisnis Digital.

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

## Cara Menjalankan Program

1. Pastikan Python sudah terinstal di komputer Anda
2. Unduh file `faktorial_rekursif.py`
3. Buka terminal atau command prompt
4. Navigasikan ke direktori tempat file tersebut berada
5. Jalankan perintah: `python faktorial_rekursif.py`
6. Ikuti instruksi di layar untuk memasukkan angka

## Contoh Output Program

```
Masukkan angka untuk dihitung faktorialnya: 5
Faktorial dari 5 adalah 120
```

## Catatan Pembelajaran

Fungsi rekursif faktorial ini merupakan contoh sederhana namun kuat untuk memahami konsep rekursi dalam pemrograman. Konsep ini menjadi dasar untuk memahami algoritma-algoritma yang lebih kompleks seperti traversal tree, backtracking, dan dynamic programming.

Dalam konteks bisnis digital, pemahaman fungsi rekursif membantu dalam pengembangan algoritma untuk:
- Analisis struktur data kompleks
- Pengolahan data hierarkis
- Optimisasi proses bisnis
- Pengembangan sistem cerdas
