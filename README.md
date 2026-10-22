
# SIMULASI MONTE CARLO UNTUK MEMPERKIRAKAN JUMLAH ITEM YANG TERJUAL PADA SEBUAH TOKO ROTI MENGGUNAKAN BAHASA R

**Nama:** Fatimatuzahro Juliawati  
**NIM:** 2311060063  
**Mata Kuliah:** Simulasi dan Pemodelan (Simulasi Monte Carlo)

## 1. Deskripsi Kasus

Jumlah roti yang terjual per hari pada sebuah toko roti (French Bakery) tidak selalu tetap karena jumlah pembelian bisa berubah-ubah. Untuk memperkirakan penjualan tersebut, digunakan metode Simulasi Monte Carlo dengan memanfaatkan data penjualan sebelumnya.

Simulasi ini bertujuan untuk mengetahui rata-rata penjualan harian dan melihat kemungkinan total penjualan selama 30 hari.

## 2. Sumber Data dan Bahasa Pemrograman

**Sumber dataset:** [French Bakery Daily Sales (Kaggle)](https://www.kaggle.com/datasets/matthieugimbert/french-bakery-daily-sales)

Dataset awal dianalisis menggunakan **Python di Google Colab** untuk memperoleh total penjualan harian sebelum disimulasikan menggunakan **bahasa R**.

Dari total **600 catatan penjualan harian**, diperoleh nilai kuartil pertama (Q1) sebesar **366 item** dan kuartil ketiga (Q3) sebesar **780,75 item**. Selanjutnya, data dikelompokkan menjadi tiga kondisi penjualan:

| Kondisi | Frekuensi | Rata-rata Item Terjual |
|:--|--:|--:|
| Sepi | 149 hari | 306,10 |
| Sedang | 301 hari | 511,98 |
| Ramai | 150 hari | 1.068,49 |
| **Total** | **600 hari** | — |

## 3. Metode Simulasi Monte Carlo

Langkah-langkah yang dilakukan dalam simulasi:

1. Menentukan distribusi probabilitas.
2. Menghitung probabilitas kumulatif.
3. Menentukan interval bilangan acak 1–100.
4. Melakukan 1.000 percobaan Monte Carlo.
5. Melakukan 1.000 skenario penjualan selama 30 hari.

Tabel probabilitas, probabilitas kumulatif, dan interval bilangan acak yang telah dibulatkan:

| Kondisi | Probabilitas | Probabilitas Kumulatif | Interval Acak |
|:--|--:|--:|:--|
| Sepi | 0,25 | 0,25 | 1–25 |
| Sedang | 0,50 | 0,75 | 26–75 |
| Ramai | 0,25 | 1,00 | 76–100 |

## 4. Hasil Simulasi

Setelah dilakukan **1.000 percobaan simulasi**, hasil yang diperoleh adalah:

| Kondisi | Hasil |
|:--|--:|
| Rata-rata simulasi | 602,69 item/hari |
| Rata-rata teoritis | 599,64 item/hari |
| Selisih | 0,51% |

Hasil simulasi Monte Carlo menunjukkan rata-rata penjualan harian sebesar **602,69 item**, sedangkan hasil perhitungan teoritis sebesar **599,64 item**. Selisih keduanya sekitar **0,51%**, sehingga hasil simulasi cukup mendekati nilai teoritis.

### Grafik Frekuensi Kondisi Penjualan dan Total Penjualan Selama 30 Hari

![Grafik frekuensi kondisi penjualan dan total penjualan selama 30 hari](grafik_simulasi.png)

## 5. Kesimpulan

Simulasi Monte Carlo menghasilkan rata-rata penjualan harian sebesar **602,69 item**. Angka ini sangat dekat dengan rata-rata teoritis sebesar **599,64 item**, dengan selisih **0,51%**.

Untuk periode 30 hari, jumlah penjualan yang dihasilkan simulasi berbeda-beda pada setiap percobaan, tetapi umumnya berada di sekitar **18.000 item**. Hasil tersebut mendekati perhitungan teoritis sebesar **17.989,11 item**.

Berdasarkan hasil tersebut, metode Monte Carlo dapat digunakan untuk memperkirakan jumlah penjualan roti dengan mempertimbangkan kemungkinan perubahan jumlah penjualan setiap harinya.
