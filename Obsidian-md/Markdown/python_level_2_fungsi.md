# ⚙️ Level 2: Fungsi & Modularitas

> Setelah kamu paham dasar Python, sekarang waktunya belajar cara menulis kode yang rapi, bisa dipakai ulang, dan gak bikin kamu pusing sendiri. Di sinilah kamu mulai berpikir seperti *developer*, bukan cuma pengetik cepat.

---

## 🎯 Tujuan Akhir Level 2
- Mengerti apa itu **fungsi (function)** dan kenapa penting.
- Bisa menulis fungsi sendiri dengan parameter dan nilai balik.
- Paham perbedaan antara **scope lokal** dan **global**.
- Tahu cara memakai dan membuat **modul** sendiri.

---

## 🧩 1. Apa Itu Fungsi?
Bayangin kamu punya tugas nyapu rumah. Kalau tiap hari kamu jelasin langkah-langkahnya dari awal, capek sendiri kan? Nah, fungsi itu kayak bikin *shortcut*. Kamu cukup tulis langkah-langkahnya sekali, lalu panggil kalau dibutuhkan.

Contoh sederhana:
```python
def sapa():
    print("Halo dunia!")

# panggil fungsinya
sapa()
```

Python bakal menjalankan isi fungsi **hanya ketika kamu panggil**.

---

## 🧱 2. Parameter dan Argumen
Kadang kamu butuh fungsi yang lebih fleksibel. Misalnya, sapaan yang bisa berubah nama:

```python
def sapa(nama):
    print("Halo,", nama)

sapa("Rizky")
sapa("Nadia")
```

- **Parameter**: nama variabel di dalam fungsi (`nama`).
- **Argumen**: nilai yang kamu kirim waktu memanggil fungsi (`"Rizky"`).

### Lebih dari satu parameter
```python
def tambah(a, b):
    print(a + b)

tambah(5, 3)
```

---

## 🎁 3. Nilai Kembali (Return)
Kadang kamu gak mau cuma `print()`, tapi mau fungsi **mengembalikan hasil** buat dipakai lagi.

```python
def kali(a, b):
    return a * b

hasil = kali(4, 5)
print(hasil)
```

Bedanya `print()` dan `return`:
- `print()` cuma menampilkan di layar.
- `return` menyimpan hasil agar bisa dipakai di tempat lain.

Analogi gampangnya: `print()` kayak ngomong keras-keras, `return` kayak nyatet di buku buat dipakai lagi nanti.

---

## 🧠 4. Scope Variabel (Lokal vs Global)
Scope itu jangkauan hidup sebuah variabel.

```python
x = 10  # variabel global

def ubah():
    x = 5  # variabel lokal
    print("Di dalam fungsi:", x)

ubah()
print("Di luar fungsi:", x)
```

Outputnya:
```
Di dalam fungsi: 5
Di luar fungsi: 10
```

Variabel `x` di dalam fungsi hanya hidup di sana, gak ngaruh ke luar.
Kalau kamu mau ubah variabel global secara langsung:
```python
def ubah_global():
    global x
    x = 99
```
Tapi hati-hati, pakai `global` terlalu sering bikin kode susah dilacak.

---

## 🧩 5. Fungsi dengan Nilai Default
Kamu bisa kasih nilai default ke parameter supaya gak wajib diisi.
```python
def sapa(nama="Anonim"):
    print("Halo,", nama)

sapa()       # Halo, Anonim
sapa("Rizky") # Halo, Rizky
```

---

## 🧱 6. Fungsi di Dalam Fungsi
Kamu bisa bikin fungsi yang memanggil fungsi lain.
```python
def hitung_luas_persegi(sisi):
    return sisi * sisi

def tampilkan_luas(sisi):
    luas = hitung_luas_persegi(sisi)
    print("Luas persegi adalah", luas)

tampilkan_luas(4)
```
Ini bikin kode kamu terstruktur dan gampang dibaca.

---

## 📦 7. Modularitas: Pisahkan Kode Jadi Modul
Setelah fungsi-fungsimu banyak, jangan semua ditaruh di satu file.

Buat file baru bernama `math_utils.py`:
```python
def tambah(a, b):
    return a + b

def kali(a, b):
    return a * b
```

Lalu di file utama `main.py`:
```python
import math_utils

print(math_utils.tambah(3, 4))
print(math_utils.kali(2, 5))
```

Kalau mau panggil cuma fungsi tertentu:
```python
from math_utils import tambah
print(tambah(10, 5))
```

Modul = cara Python nyimpen fungsi dalam file biar bisa dipakai di proyek lain.

---

## 🧩 8. Built-in Functions
Python udah punya banyak fungsi bawaan, contohnya:
```python
len([1, 2, 3])   # 3
max([10, 20, 5]) # 20
min([10, 20, 5]) # 5
abs(-10)         # 10
round(3.1415, 2) # 3.14
```
Kamu bisa pakai tanpa harus bikin sendiri.

---

## 🧠 9. Latihan Level 2
1. Buat fungsi `hitung_diskon(harga, persen)` yang mengembalikan harga setelah diskon.
2. Buat modul `konversi.py` berisi fungsi `c_to_f()` dan `f_to_c()`.
3. Buat program utama yang mengimpor `konversi.py` dan minta input suhu dari user.
4. Buat fungsi `is_genap(angka)` yang mengembalikan `True` jika angka genap.

---

## ✅ Target Akhir Level 2
- Bisa menulis dan memakai fungsi dengan parameter & return value.
- Bisa memisahkan kode ke modul terpisah.
- Kode kamu mulai rapi, reusable, dan lebih profesional.

Kalau sudah paham dan lancar di sini, baru lanjut ke **Level 3: Pemrograman Berorientasi Objek (OOP)** — bagian yang bikin kamu benar-benar bisa berpikir seperti programmer beneran.

