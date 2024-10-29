# Penanganan Kesalahan di Python

Penanganan kesalahan adalah bagian penting dari pemrograman karena membantu kita mengatasi kesalahan yang mungkin terjadi selama runtime, sehingga program tidak berhenti secara tiba-tiba. Python menyediakan beberapa cara untuk menangani kesalahan seperti `raise`, `assert`, dan blok `try`/`except`. Mari kita bahas konsep-konsep ini satu per satu.

## 1. Blok Try dan Except
Blok `try` dan `except` digunakan untuk menangani kesalahan yang mungkin terjadi saat program dijalankan. Jika suatu kode di dalam blok `try` menimbulkan kesalahan, maka blok `except` akan menangani kesalahan tersebut tanpa membuat program berhenti.

**Sintaks:**
```python
try:
    # kode yang mungkin menimbulkan kesalahan
except ExceptionType:
    # kode untuk menangani kesalahan tersebut
```

**Contoh:**
```python
try:
    angka = int(input("Masukkan sebuah angka: "))
    hasil = 10 / angka
    print("Hasilnya adalah:", hasil)
except ZeroDivisionError:
    print("Tidak bisa membagi dengan nol!")
except ValueError:
    print("Input harus berupa angka.")
except AssertionError:
    print("Terjadi AssertionError!")
except FileNotFoundError:
    print("File yang diminta tidak ditemukan!")
except IndexError:
    print("Index yang diakses berada di luar batas!")
except KeyError:
    print("Kunci yang diminta tidak ditemukan dalam dictionary!")
except TypeError:
    print("Operasi atau fungsi diterapkan pada tipe yang tidak sesuai!")
except Exception as e:
    print(f"Kesalahan yang tidak terduga terjadi: {e}")
```

- **Penjelasan**:
  - Blok `try` berisi kode yang mungkin menimbulkan kesalahan.
  - Jika pengguna memasukkan `0`, maka `ZeroDivisionError` akan terjadi dan ditangani oleh blok `except` yang sesuai.
  - Jika pengguna memasukkan input yang bukan angka, `ValueError` akan terjadi, dan blok `except` yang sesuai akan menangani kesalahan tersebut.
  - Blok `except` lainnya menangani berbagai kesalahan seperti `AssertionError`, `FileNotFoundError`, `IndexError`, `KeyError`, `TypeError`, dan kesalahan lainnya dengan `Exception`.

**Beberapa Contoh Kesalahan Umum**:
- `ZeroDivisionError` - Kesalahan pembagian dengan nol.
- `ValueError` - Kesalahan jika konversi tipe data gagal, misalnya `int('abc')`.
- `FileNotFoundError` - Kesalahan jika file yang dicari tidak ditemukan.
- `IndexError` - Kesalahan jika mencoba mengakses indeks yang tidak ada dalam suatu list atau tuple.
- `KeyError` - Kesalahan jika kunci yang diminta tidak ada dalam dictionary.
- `TypeError` - Kesalahan jika operasi atau fungsi diterapkan pada tipe data yang tidak sesuai.
- `AssertionError` - Kesalahan jika pernyataan `assert` gagal.

## 2. Raise
`raise` digunakan untuk secara manual menimbulkan kesalahan (error). Terkadang, kita ingin menimbulkan kesalahan sendiri untuk memastikan bahwa kode kita bekerja seperti yang diharapkan.

**Sintaks:**
```python
raise ExceptionType("Pesan kesalahan")
```

**Contoh:**
```python
def cek_umur(umur):
    if umur < 0:
        raise ValueError("Umur tidak bisa negatif!")
    else:
        print("Umur valid:", umur)

try:
    cek_umur(-5)
except ValueError as e:
    print("Kesalahan:", e)
```

- **Penjelasan**:
  - Fungsi `cek_umur()` memeriksa apakah umur bernilai negatif.
  - Jika `umur` negatif, `raise` digunakan untuk menimbulkan `ValueError` dengan pesan "Umur tidak bisa negatif!".
  - Dalam blok `try`, kesalahan ini ditangkap oleh blok `except`, dan pesan kesalahan ditampilkan.

## 3. Assert
`assert` digunakan untuk melakukan verifikasi atau pengecekan tertentu selama eksekusi. Jika ekspresi di dalam `assert` bernilai `False`, Python akan menimbulkan kesalahan `AssertionError`. Ini berguna untuk debugging dan memastikan bahwa asumsi tertentu dalam kode adalah benar.

**Sintaks:**
```python
assert kondisi, "Pesan kesalahan jika kondisi False"
```

**Contoh:**
```python
def bagi(angka1, angka2):
    assert angka2 != 0, "Pembagi tidak boleh nol!"
    return angka1 / angka2

try:
    print(bagi(10, 0))
except AssertionError as e:
    print("Kesalahan:", e)
```

- **Penjelasan**:
  - Pada contoh di atas, `assert` memastikan bahwa `angka2` tidak boleh nol sebelum operasi pembagian dilakukan.
  - Jika `angka2` adalah `0`, maka `AssertionError` akan ditimbulkan dengan pesan "Pembagi tidak boleh nol!".

## Detail Blok Try dan Except dengan Else dan Finally
Blok `try` juga dapat dikombinasikan dengan blok `else` dan `finally` untuk menambahkan logika yang lebih baik dalam penanganan kesalahan.

- **`else`**: Dijalankan jika tidak ada kesalahan di dalam blok `try`.
- **`finally`**: Dijalankan baik kesalahan terjadi maupun tidak (biasanya digunakan untuk melakukan pembersihan, seperti menutup file).

**Contoh:**
```python
try:
    angka = int(input("Masukkan sebuah angka: "))
    hasil = 10 / angka
except ZeroDivisionError:
    print("Tidak bisa membagi dengan nol!")
except ValueError:
    print("Input harus berupa angka.")
else:
    print("Pembagian berhasil, hasilnya adalah:", hasil)
finally:
    print("Blok finally selalu dieksekusi.")
```

- **Penjelasan**:
  - Blok `else` hanya dieksekusi jika tidak ada kesalahan di dalam blok `try`.
  - Blok `finally` akan dieksekusi baik ada kesalahan maupun tidak, misalnya untuk melakukan pembersihan sumber daya.

## Studi Kasus: Penanganan Kesalahan pada Pengisian Data
Misalkan kita membuat sebuah program untuk memproses data pengguna. Kita akan menggabungkan semua konsep yang telah dipelajari.

**Contoh:**
```python
def input_umur():
    while True:
        try:
            umur = int(input("Masukkan umur Anda: "))
            if umur < 0:
                raise ValueError("Umur tidak boleh negatif.")
            break
        except ValueError as e:
            print("Kesalahan:", e)
            print("Coba lagi...\n")
    return umur

umur = input_umur()
print("Umur Anda adalah:", umur)
```

- **Penjelasan**:
  - Fungsi `input_umur()` meminta input umur dari pengguna.
  - Jika pengguna memasukkan angka yang tidak valid (misalnya negatif atau bukan angka), maka blok `except` menangkap `ValueError` dan meminta pengguna untuk mencoba lagi.

## Task
Untuk mengasah pemahaman tentang penanganan kesalahan, cobalah beberapa latihan berikut:
1. Buat fungsi yang meminta pengguna memasukkan nama file dan membaca isinya. Tangani kesalahan jika file tidak ditemukan (`FileNotFoundError`).
2. Buat fungsi yang melakukan operasi matematika antara dua angka, dan tangani beberapa kesalahan seperti `ZeroDivisionError` dan `ValueError`.
3. Implementasikan `assert` dalam sebuah fungsi yang memastikan bahwa nilai input harus berada dalam rentang tertentu (misalnya 1 sampai 100).
