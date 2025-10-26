# 🧱 Level 1: Dasar-Dasar Python

> Ini pondasi utama sebelum kamu bisa ngoding dengan percaya diri. Fokusnya di logika dasar, cara kerja Python, dan membiasakan otak berpikir seperti komputer.

---

## 🎯 Tujuan Akhir Level 1
- Paham apa itu **variabel, tipe data, operator, input/output**.
- Bisa menulis program sederhana tanpa error dasar.
- Ngerti gimana komputer memproses instruksi baris demi baris.

---

## 🧩 1. Konsep Dasar Python
Python itu kayak bahasa manusia tapi sedikit lebih disiplin. Kalau kamu bisa kasih instruksi yang jelas dan berurutan, dia nurut. Kalau salah titik koma, dia marah.

Contoh kode pertama (tradisi wajib semua programmer):
```python
print("Hello, World!")
```
Python baca ini dari atas ke bawah, kiri ke kanan. Gak ada tanda titik koma di akhir, cukup baris baru.

---

## 📦 2. Variabel
Variabel itu kayak kotak penyimpanan yang kamu kasih label.

Bayangin kamu punya laci bernama `umur`. Kamu bisa masukin angka ke dalamnya:
```python
umur = 17
```
Sekarang kapan pun kamu butuh umur, tinggal panggil:
```python
print(umur)
```

### Aturan penting:
- Nama variabel gak boleh diawali angka (`2angka` salah, `angka2` benar).
- Gak boleh ada spasi (`total harga` salah, `total_harga` benar).
- Case sensitive (`nama` beda sama `Nama`).

---

## 🔢 3. Tipe Data Dasar
Python punya beberapa tipe data utama:

| Tipe | Contoh | Keterangan |
|------|---------|------------|
| `int` | 10 | Angka bulat |
| `float` | 3.14 | Angka desimal |
| `str` | "Halo" | Teks (string) |
| `bool` | True / False | Logika benar/salah |

Cek tipe data dengan:
```python
print(type(umur))
```

Analoginya: bayangin kamu punya label di kotak. Kalau isinya "pisang", kamu gak bisa langsung pakai buat operasi matematika. Begitu juga Python — kalau kamu nyoba nambahin teks dan angka, dia bingung.

---

## 🧮 4. Operator
Operator itu alat buat ngelakuin operasi di variabel atau nilai.

### Aritmatika
```python
a = 10
b = 3
print(a + b)  # tambah
print(a - b)  # kurang
print(a * b)  # kali
print(a / b)  # bagi (hasil desimal)
print(a // b) # bagi (hasil bulat)
print(a % b)  # sisa bagi
print(a ** b) # pangkat
```

### Perbandingan
```python
print(a > b)  # lebih besar
print(a == b) # sama dengan
print(a != b) # tidak sama
```

### Logika (Boolean)
```python
x = True
y = False
print(x and y)  # True kalau dua-duanya True
print(x or y)   # True kalau salah satu True
print(not x)    # kebalikan nilai x
```

---

## 🗣️ 5. Input & Output
Kalau kamu mau programmu interaktif, kamu pakai `input()`.
```python
nama = input("Masukkan nama kamu: ")
print("Halo,", nama)
```

Tapi hati-hati, `input()` **selalu ngasih string**. Jadi kalau mau pakai angka:
```python
umur = int(input("Masukkan umur kamu: "))
print("Tahun depan umur kamu", umur + 1)
```
Kalau kamu lupa ubah jadi `int`, Python bakal protes karena gak bisa nambahin teks dan angka.

---

## 🔄 6. Casting (Ubah Tipe Data)
Kadang kamu butuh ubah tipe data manual:
```python
angka = "10"
print(type(angka))  # str
angka = int(angka)
print(type(angka))  # int
```
Analogi: kayak ngubah gelas jus jadi gelas kopi — isinya tetap cairan, tapi bentuk wadahnya disesuaikan biar bisa dipakai di tempat lain.

---

## ⚙️ 7. Struktur Kontrol (If-Else)
Bagian ini bikin program kamu bisa *berpikir*.

```python
umur = int(input("Masukkan umur kamu: "))
if umur >= 18:
    print("Kamu sudah dewasa.")
elif umur > 12:
    print("Kamu remaja.")
else:
    print("Kamu masih anak-anak.")
```
Python membaca dari atas ke bawah, dan berhenti di kondisi yang benar pertama kali.

---

## 🔁 8. Looping (Perulangan)
Ulangi sesuatu tanpa harus ngetik berulang.

### For loop
```python
for i in range(5):
    print("Halo ke-", i)
```

### While loop
```python
hitung = 0
while hitung < 5:
    print("Angka ke-", hitung)
    hitung += 1
```
`while` jalan terus sampai kondisi salah.

---

## 📚 9. Struktur Data Dasar
### List
Tempat nyimpen banyak nilai sekaligus.
```python
buah = ["apel", "pisang", "jeruk"]
print(buah[0])  # akses elemen pertama
```

### Tuple
Kayak list tapi gak bisa diubah.
```python
angka = (1, 2, 3)
```

### Set
Kumpulan unik, gak ada duplikat.
```python
warna = {"merah", "biru", "merah"}
print(warna)  # hanya muncul sekali
```

### Dictionary
Kumpulan pasangan kunci-nilai.
```python
siswa = {"nama": "Rizky", "umur": 18}
print(siswa["nama"])
```

---

## 🧠 Latihan Level 1
1. Buat program konversi suhu (Celsius ke Fahrenheit).
2. Buat program kalkulator sederhana.
3. Program cek genap/ganjil dari input angka.
4. Program daftar belanja dengan `list`.

---

## ✅ Target Akhir Level 1
- Paham dan bisa pakai tipe data dasar.
- Bisa ngambil input dari user dan tampilkan hasilnya.
- Gak panik lihat error sederhana.

Kalau kamu udah nyaman di sini, baru lanjut ke **Level 2: Fungsi & Modularitas**.

