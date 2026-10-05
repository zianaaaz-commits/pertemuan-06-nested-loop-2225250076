# Pertemuan 06 Nested Loop Python

Nama: Ziana Alfia Zahra
NIM: 2225250076
Kelas: 3A

## Tujuan

Menggunakan nested loop, pola, akumulasi, dan pencacahan.

## Cara Menjalankan

Program dijalankan menggunakan Python melalui VS Code.

Untuk menjalankan Tugas 3, gunakan perintah:

```bash
python3 tugas/tabel_perkalian_dan_statistik.py
```

Kemudian masukkan nilai `n` berupa bilangan bulat positif.

## Algoritma Tugas 3

Program menerima nilai `n` sebagai bilangan bulat positif. Jika `n` kurang dari atau sama dengan 0, program meminta input kembali sampai mendapatkan nilai yang valid.

Loop luar digunakan untuk mengatur nilai `i` dari 1 sampai `n`, sedangkan loop dalam digunakan untuk mengatur nilai `j` dari 1 sampai `n`.

Pada setiap pasangan `i` dan `j`, program menghitung:

```python
hasil = i * j
```

`total_baris` digunakan sebagai akumulator untuk menjumlahkan hasil pada setiap baris.

`total_semua` digunakan sebagai akumulator untuk menjumlahkan seluruh hasil perkalian.

`count_genap` digunakan sebagai counter untuk menghitung banyak hasil perkalian yang bernilai genap.

## Hasil Pengujian

| Input | Hasil yang Diharapkan                                         | Keluaran Aktual                                               | Status   |
| ----- | ------------------------------------------------------------- | ------------------------------------------------------------- | -------- |
| n = 1 | Jumlah pasangan = 1, Total semua = 1, Banyak hasil genap = 0  | Jumlah pasangan = 1, Total semua = 1, Banyak hasil genap = 0  | Berhasil |
| n = 2 | Jumlah pasangan = 4, Total semua = 9, Banyak hasil genap = 3  | Jumlah pasangan = 4, Total semua = 9, Banyak hasil genap = 3  | Berhasil |
| n = 3 | Jumlah pasangan = 9, Total semua = 36, Banyak hasil genap = 5 | Jumlah pasangan = 9, Total semua = 36, Banyak hasil genap = 5 | Berhasil |

## Analisis Efisiensi

Untuk setiap nilai `i`, loop dalam berjalan sebanyak `n` kali. Karena loop luar juga berjalan sebanyak `n` kali, maka badan loop dalam berjalan sebanyak:

`n × n = n²` kali.

Pernyataan `hasil = i * j` juga dieksekusi sebanyak `n²` kali.

## Refleksi

Kesalahan yang dapat terjadi pada nested loop adalah salah menempatkan `total_baris = 0`. Jika variabel tersebut tidak direset pada setiap awal baris, hasil penjumlahan dari baris sebelumnya akan ikut terbawa ke baris berikutnya.

Perbaikannya adalah menempatkan `total_baris = 0` di dalam loop luar, sebelum loop dalam dijalankan.