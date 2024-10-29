# Membaca dan Menulis Berkas di Python

Bekerja dengan berkas (file) adalah salah satu keterampilan penting dalam pemrograman. Python menyediakan berbagai cara untuk membaca dan menulis berkas dengan menggunakan fungsi bawaan. Pada materi ini, kita akan belajar bagaimana menggunakan fungsi `open()` untuk membuka, membaca, menulis, dan menutup berkas dalam Python. Durasi materi ini sekitar 45 menit.

## 1. Membuka Berkas dengan Fungsi `open()`
Sebelum membaca atau menulis berkas, kita harus membukanya terlebih dahulu menggunakan fungsi `open()`. Fungsi `open()` ini memungkinkan kita menentukan mode bagaimana berkas akan dibuka. Berikut adalah beberapa mode yang dapat digunakan:

- **Mode Baca (`'r'`)**: Membaca berkas. Jika berkas tidak ditemukan, Python akan menimbulkan `FileNotFoundError`.
- **Mode Tulis (`'w'`)**: Menulis ke berkas. Jika berkas sudah ada, isinya akan ditimpa. Jika berkas belum ada, Python akan membuat berkas baru.
- **Mode Tambah (`'a'`)**: Menambahkan data ke berkas. Jika berkas belum ada, Python akan membuat berkas baru.
- **Mode Baca dan Tulis (`'r+'`)**: Membaca dan menulis berkas. Berkas harus sudah ada.

**Contoh: Membuka Berkas dengan `open()`**
```python
# Membuka berkas dalam mode baca ('r')
file = open('contoh.txt', 'r')
```

- **Penjelasan**:
  - `open('contoh.txt', 'r')` membuka berkas `contoh.txt` dalam mode baca. Jika berkas tidak ditemukan, Python akan menimbulkan `FileNotFoundError`.

## 2. Membaca Berkas dengan `open()`
Setelah berkas dibuka, kita dapat membacanya. Fungsi `open()` menyediakan beberapa metode untuk membaca berkas di Python, seperti:

- **`read()`**: Membaca seluruh isi berkas.
- **`readline()`**: Membaca satu baris dari berkas.
- **`readlines()`**: Membaca seluruh baris dalam berkas dan mengembalikannya dalam bentuk list.

**Contoh: Membaca Berkas**
```python
# Membuka berkas dalam mode baca
file = open('contoh.txt', 'r')

# Membaca seluruh isi berkas
isi_berkas = file.read()
print(isi_berkas)

# Jangan lupa untuk menutup berkas
file.close()
```

- **Penjelasan**:
  - `file.read()` membaca seluruh isi berkas dan mengembalikannya sebagai string.
  - Jangan lupa menutup berkas menggunakan `file.close()` untuk membebaskan sumber daya.

**Membaca Berkas Baris per Baris**
```python
file = open('contoh.txt', 'r')

# Membaca baris demi baris
for baris in file:
    print(baris.strip())  # .strip() untuk menghapus karakter newline di akhir baris

file.close()
```
- **Penjelasan**:
  - Kita bisa menggunakan loop `for` untuk membaca setiap baris dalam berkas.
  - `strip()` digunakan untuk menghapus karakter newline (`\n`) di akhir setiap baris.

## 3. Menulis ke Berkas dengan `open()`
Kita juga dapat menulis ke berkas menggunakan fungsi `write()`. Untuk menulis ke berkas, kita harus membukanya dalam mode tulis (`'w'`) atau mode tambah (`'a'`).

**Contoh: Menulis ke Berkas**
```python
# Membuka berkas dalam mode tulis
file = open('contoh.txt', 'w')

# Menulis ke berkas
file.write("Halo, ini adalah baris pertama.\n")
file.write("Ini adalah baris kedua.\n")

# Jangan lupa untuk menutup berkas
file.close()
```

- **Penjelasan**:
  - Mode `'w'` akan membuat berkas baru jika berkas belum ada, atau menimpa berkas jika sudah ada.
  - `write()` digunakan untuk menulis string ke dalam berkas. Untuk membuat baris baru, tambahkan karakter newline (`\n`).

**Menambahkan ke Berkas (Append) dengan `open()`**
```python
# Membuka berkas dalam mode tambah
file = open('contoh.txt', 'a')

# Menambahkan teks ke berkas
file.write("Ini adalah baris tambahan.\n")

file.close()
```

- **Penjelasan**:
  - Mode `'a'` digunakan untuk menambahkan teks ke akhir berkas tanpa menghapus isi yang sudah ada.

## 4. Menggunakan Blok `with` untuk Mengelola Berkas
Penggunaan `open()` harus diikuti dengan `close()` untuk menutup berkas secara manual, yang terkadang dapat dilupakan. Python menyediakan cara yang lebih aman untuk membuka berkas menggunakan blok `with`. Setelah keluar dari blok `with`, Python akan otomatis menutup berkas tersebut.

**Contoh: Membaca dan Menulis dengan Blok `with`**
```python
# Membaca berkas menggunakan blok with
with open('contoh.txt', 'r') as file:
    isi_berkas = file.read()
    print(isi_berkas)

# Menulis ke berkas menggunakan blok with
with open('contoh.txt', 'w') as file:
    file.write("Menulis teks dengan aman menggunakan blok with.\n")
```

- **Penjelasan**:
  - Menggunakan `with open(...) as file:` akan membuka berkas dan memastikan berkas tersebut ditutup secara otomatis setelah blok kode selesai dieksekusi.

## 5. Membaca dan Menulis Berkas CSV dengan `open()`
Selain berkas teks biasa, Python juga sering digunakan untuk bekerja dengan berkas CSV. Python menyediakan modul `csv` untuk mempermudah pembacaan dan penulisan berkas CSV.

**Contoh: Membaca Berkas CSV**
```python
import csv

with open('data.csv', 'r') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print(row)
```

- **Penjelasan**:
  - Menggunakan `csv.reader()` untuk membaca berkas CSV baris per baris.

**Contoh: Menulis ke Berkas CSV**
```python
import csv

with open('data.csv', 'w', newline='') as csvfile:
    writer = csv.writer(csvfile)
    writer.writerow(['Nama', 'Umur', 'Kota'])
    writer.writerow(['Alice', 30, 'Jakarta'])
    writer.writerow(['Bob', 25, 'Bandung'])
```

- **Penjelasan**:
  - Menggunakan `csv.writer()` untuk menulis data ke berkas CSV.
  - `newline=''` digunakan untuk menghindari baris kosong tambahan yang mungkin terjadi saat menulis ke CSV.

## 6. Summary
- Fungsi `open()` digunakan untuk membuka berkas dalam mode baca (`'r'`), tulis (`'w'`), atau tambah (`'a'`).
- Selalu ingat untuk menutup berkas menggunakan `close()`, atau gunakan blok `with` agar berkas otomatis ditutup.
- Ada berbagai cara untuk membaca berkas setelah dibuka dengan `open()`, seperti menggunakan `read()`, `readline()`, atau membaca baris per baris.
- Penulisan ke berkas dapat dilakukan dengan mode `'w'` untuk menimpa atau `'a'` untuk menambahkan isi ke berkas.
- Python menyediakan modul `csv` untuk memudahkan pembacaan dan penulisan berkas CSV menggunakan `open()`.
