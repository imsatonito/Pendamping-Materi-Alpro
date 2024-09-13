**Python Syntax - Print Function**
=====================================

### Menampilkan Hasil dalam Program Menggunakan Fungsi `print()`

Fungsi `print()` dalam bahasa pemrograman Python adalah sebuah command untuk menampilkan hasil di dalam program.

#### Contoh Penggunaan Fungsi `print()`

Untuk menampilkan sebuah karakter atau kalimat menggunakan fungsi `print()`, maka karakter atau kalimat tersebut harus dilingkupi dengan tanda kutip (`""`).

```python
print("Hello World!")
```

**Output**
```
Hello World!
```

#### Mencetak Nilai Numerik

Untuk mencetak nilai numerik, masukkan angka tanpa tanda kutip.

```python
print(10)
print(7.5)
```

**Output**
```
10
7.5
```

#### Menggabungkan String dan Angka

Anda juga dapat menggabungkan string dan angka dengan operator koma.

```python
print("Hello", 10)
```

**Output**
```
Hello 10
```

#### Menggunakan Operator `*` dan `+`

```python
print("Hello" * 3)  # akan menduplicate string "Hello" sebanyak 3 kali
print(10 * 20)  # akan mengalikan bilangan tersebut

print("Hello" + "World")  # akan menggabungkan kedua string tersebut
print(10 + 20)  # akan menambahkan kedua bilangan tersebut
```

**Output**
```
HelloHelloHello
200
Hello World
30
```

#### Peringatan!

Operator `+` tidak bisa digunakan untuk 2 tipe data yang digabungkan seperti string dan integer.

```python
print("Hello" + 3)  # akan muncul error
```
<br><br><br><br>

**Python Syntax - Comment**
==========================

### Komentar dalam Program

Komentar dalam program merupakan bagian yang cukup penting untuk memberi tahu maksud dan tujuan dari program tersebut. Komentar merupakan bagian dari program yang tidak akan dieksekusi oleh sistem.

### Tipe Komentar di Python

Dalam bahasa pemrograman Python, terdapat dua tipe komentar:

* **Single Line Comment**: Digunakan untuk memberi komentar pada satu baris kode.
* **Multiple Line Comment**: Digunakan untuk memberi komentar pada beberapa baris kode.

### Sintaks Komentar

Untuk memberi komentar, kita menggunakan sintaks `#` untuk single-line comment atau `"""` untuk multi-line comment.

### Contoh Komentar

```python
""" Program ini bertujuan untuk
      menampilkan angka 5 
      dengan menggunakan fungsi print """

print(5)  # Menampilkan angka 5
```

Dalam contoh di atas, kita menggunakan `"""` untuk memberi komentar pada beberapa baris kode, dan `#` untuk memberi komentar pada satu baris kode.

### Penggunaan Komentar

Komentar sangat berguna untuk:

* Membantu orang lain memahami kode program
* Membantu diri sendiri memahami kode program yang telah ditulis
* Membuat kode program lebih mudah dibaca dan dipahami

Dengan menggunakan komentar, kita dapat membuat kode program lebih jelas dan lebih mudah dipahami.

<br><br><br><br>

**Klasifikasi Tipe Data di Python**
=====================================

### Operator dan Tipe Data

Dalam Python, operator berlaku berbeda tergantung pada tipe data. Contohnya, hasil operasi perkalian `*` bilangan 100 dan 2 adalah 200, tetapi hasil operasi perkalian string `'100'` dan `'2'` adalah `'100100'`.

### Tipe Data Python

Berikut adalah rangkuman struktur data dalam bahasa Python yang penting dan akan terus dipakai selama kelas ini:

### Basic Data Types

* **Number**: Tipe data numerik, seperti integer dan float.
* **Boolean**: Tipe data logika, seperti True dan False.
* **String**: Tipe data teks, seperti `'Halo'` dan `'Selamat pagi'`.
* **List**: Tipe data koleksi, seperti `[1, 2, 3]` dan `['a', 'b', 'c']`.
* **Tuple**: Tipe data koleksi yang tidak dapat berubah, seperti `(1, 2, 3)` dan `('a', 'b', 'c')`.
* **Dictionary**: Tipe data koleksi yang berisi pasangan kunci dan nilai, seperti `{'nama': 'John', 'umur': 30}`.

### Contoh Operasi Perkalian

* `100 * 2 = 200` (operasi perkalian numerik)
* `'100' * 2 = '100100'` (operasi perkalian string)
* `'Halo' * 2 = 'HaloHalo'` (operasi perkalian string)

Dengan memahami tipe data dan operasi yang berlaku pada masing-masing tipe data, Anda dapat menggunakan Python dengan lebih efektif dan efisien.

<br><br><br><br>

Tipe Data String
================

### Karakteristik String

Dalam Python, string sangat cocok untuk menampilkan informasi dalam perangkat lunak. Nama pengguna, ID, dan kata sandi dapat dinyatakan sebagai string. String dalam Python adalah bentuk di mana setiap huruf terhubung. Operasi penjumlahan dan perkalian dimungkinkan untuk string dalam Python. Huruf dan spasi dalam sebuah string juga disebut sebagai character.

### Operasi String

#### String Operator

Operasi `+` dan `*` yang diperbolehkan dalam string:

*   Operasi `+` dari string menghubungkan dua string menjadi satu string.
*   Operasi `*` dari string harus berupa bilangan bulat. Artinya, akan menduplikasi string tersebut atau berulang sejumlah bilangan bulat n.

```python
1. 'I' + 'Love' + 'Python!'  # String dapat ditambahkan ke string.
2. 'Python' * 10  # Menghasilkan string 'Python' diulang sebanyak 10 kali
3. '*' * 50  # Menghasilkan string '*' diulang sebanyak 50 kali
4. str(100) * 10  # String '100' diulang sebanyak 10 kali
```


### Pengindeksan String

#### Positive Index

Pengindeksan string dapat digunakan untuk mendapatkan hanya beberapa character dari string yang panjang. Gunakan tanda kurung besar `[]` dan nomor/urutan index.

Contoh:

*   Jika kita ingin mendapatkan character pertama dalam string tersebut, tidak menggunakan angka indeks 1 melainkan dimulai dari angka indeks 0.

```python
1. "hello"[0]  
   # output 'h'  
2. "hello"[2]  
   # output 'l'
```

#### Negative Index

Jika ingin mendapatkan character dihitung dari akhir dari sebuah string, maka kita dapat menggunakan tanda `-` dan dimulai dari indeks 1 untuk mendapatkan character terakhir dari string.

```python
1. "hello"[-1]  
   # output 'o'  
```

### Fungsi Built-in String

Dalam tipe data string dalam python, kita juga dapat menggunakan built-in function yang disediakan oleh python. Berikut adalah contoh-contoh:

#### `split()`

*   Digunakan untuk memisahkan string sesuai dengan separator yang kita inginkan dan mengembalikan hasilnya sebagai sebuah list.

Contoh:

```python
teks = "halo, nama saya, budi"
x = teks.split(", ")
print(x)
```

Output:

```python
['halo', 'nama saya', 'budi']
```

#### `islower()`

*   Digunakan untuk mengecek apakah semua element dalam string adalah huruf kecil, akan mengembalikan `True` jika iya, dan `False` jika tidak.

Contoh:

```python
a = "HaLo"
b = "halo"

print(a.islower())
print(b.islower())
```

Output:

```python
False
True
```

#### `count()`

*   Digunakan untuk menghitung berapa kali sebuah value muncul dalam sebuah string.

Contoh:

```python
teks = "Halo semuanya, disini saya bersama dengan budi semuanya"
x = teks.count("semuanya")
print(x)
```

Output:

```python
2
```
<br><br><br><br>

Operator Basic
================

### Konsep Operator dan Operand

Dalam pemrograman, operasi menggunakan informasi numerik dan kemudian menggunakan data tersebut sering terjadi. Misalnya, informasi seperti tinggi dan berat badan seseorang dinyatakan sebagai nilai numerik seperti 177cm dan 58kg.

Nilai data atau variabel yang akan dipakai pada operasi disebut Operand. Subjek operasi disebut Operator. Ambil contoh operasi 100 + 200.

```python
print(100 + 200) # 100 dan 200 adalah operand
```

### List Operator pada Python

Berikut beberapa operator basic yang dapat dipakai dalam bahasa pemrograman Python:

### Operator Aritmatika

| Operator | Nama Operasi | Deskripsi |
| --- | --- | --- |
| `+` | Penjumlahan | Tambahkan operand kiri dan operand kanan. |
| `-` | Pengurangan | Kurangi operand kanan dari operand kiri. |
| `*` | Perkalian | Kalikan operand kiri dan operand kanan. |
| `/` | Pembagian | Bagi operand kiri dengan operand kanan. Pembagian dalam Bahasa Python pada dasarnya mengembalikan nilai bilangan real. |
| `//` | Pembagian Bulat | Tidak seperti `/`, hasil pembagian digunakan untuk membuang titik desimal atau kurang dan hanya memperoleh bagian bilangan bulat. |
| `%` | Sisa Pembagian | Operator `%` dibaca sebagai operator modulo dan tidak ada hubungannya dengan persentase yang berarti rasio. Berguna untuk menemukan sisa pembagian. |
| `**` | Pemangkatan | Kalikan operand kiri dengan operand kanan. Dalam kasus `**0.5`, operasi akar kuadrat dilakukan.


### Penggunaan Operator

Bahasa pemrograman Python bisa digunakan untuk operasi aritmatika sederhana seperti penambahan angka, pengurangan, perkalian hingga menemukan sisa bagi dari suatu operasi pembagian. Berikut contoh penggunaan operator sederhana:

### Contoh Penggunaan Operator Aritmatika

| Operator | Contoh | Hasil |
| --- | --- | --- |
| `+` | `100 + 20` | 120 |
| `-` | `100 - 20` | 80 |
| `*` | `100 * 20` | 2000 |
| `/` | `100 / 20` | 5.0 |
| `//` | `100 // 20` | 5 |
| `%` | `100 % 20` | 0 |
| `**` | `100 ** 2` | 10000 |



### Contoh Operasi pada Python

Dalam Python, perbedaan tipe data sangat penting. Karakter dan angka memiliki bentuk yang sama, tetapi sifatnya bisa sangat berbeda.

Contoh angka 10 bisa dihitung. Namun, huruf "10" tidak mungkin bisa dihitung.

Tergantung pada tipe data, operator yang tersedia berbeda. Dalam kasus berikut, kesalahan tata bahasa terjadi karena string "10" dibagi dengan numerik 2.

```python
10 / 2
# output 5.0

'10' / 2  String 10 dibagi dengan angka 2
## TypeError
Traceback (most recent call last)
<ipython-input-40-67c5b32d2496> in <module>
----> 1 '10' / 2
# String 10 divided by number 2
TypeError: unsupported operand type(s) for /: 'str' and 'int'
```
<br><br><br><br>

### Prioritas Operator
*   Jika operator **penjumlahan** dan **perkalian** muncul dalam satu kalimat, **operasi perkalian** dilakukan terlebih dahulu.
*   Ketika **tanda kurung muncul** dalam sebuah operasi, operasi untuk operator di dalam tanda kurung **dilakukan terlebih dahulu**.
*   Hasil perhitungan dalam operasi bervariasi sesuai dengan urutan pemrosesan operator.

```python
# Contoh Perhitungan
10 + 20 * 30
Perkalian dihitung terlebih dahulu.
# output 
610

(10 + 2) * 30
Operator dalam kurung dihitung terlebih dahulu.
# output 
900
```  

Berikut urutan-urutan prioritas yang sering digunakan dalam Python (semakin tinggi posisinya dalam tabel semakin tinggi pula prioritasnya atau akan dijalankan terlebih dahulu) :
| Operator | Description |
| --- | --- |
| `()` | Parenthesis operator |
| `**` | Power operator |
| `~`, `+`, `-` | Monadic operator |
| `*`, `/`, `%`, `//` | Multiplication, division, remainder operator |
| `+`, `-` | Addition, subtraction operator |
| `>>`, `<<` | Bitwise movement operator |
| `&` | Bitwise AND operator |
| `^`, `|` | Bitwise XOR operator, bitwise OR operator |
| `<=`, `<`, `>`, `>=` | Comparison operator |
| `==`, `!=` | Equal operator |
| `=`, `%=`, `/=`, `//=`, `-=` , `+=`, `*=` , `**=` | Assignment operator, complex assignment operator |
| `is`, `is not` | Identity operator |
| `in`, `not in` | Membership test operator |
| `not`, `or`, `and` | Logical operator |

#### Priority
Semakin tinggi posisi di tabel, semakin tinggi prioritasnya.

<br><br><br><br>

# Built-in Function di Python
#### Pengenalan

Python menyediakan berbagai built-in function yang dapat membantu kita membuat program lebih ringkas dan compact. Setiap tipe data memiliki built-in function sendiri-sendiri.

#### Contoh Built-in Function

### Tipe Data Integer

* `int()`: Digunakan untuk mengubah nilai yang ditentukan menjadi bilangan bulat.

```python
x = int("12")
y = int(12.5)

print(x)
print(y)
```

Output:
```
12
12
```

### Tipe Data Float

* `pow()`: Digunakan untuk mendapatkan nilai pangkat dari suatu bilangan.

```python
x = pow(3, 3)  # 3 pangkat 3
y = pow(3, -3)  # 3 pangkat -3

print(x)
print(y)
```

Output:
```
27
0.015625
```

### Tipe Data String

* `str()`: Digunakan untuk mengubah sebuah objek menjadi string.

```python
x = str(12)
y = str(12.5)

print(type(x))
print(type(y))
```

Output:
```
<class 'str'>
<class 'str'>
```
<br><br><br><br>

# Apa itu Variabel
#### Pengenalan

Variabel adalah konsep kunci dalam pemrograman yang digunakan untuk menyimpan nilai tertentu di dalam komputer. Variabel dapat diibaratkan sebagai wadah yang dapat menyimpan nilai data.

### Karakteristik Variabel di Python

* Python tidak memerlukan deklarasi tipe data pada variabel, berbeda dengan bahasa pemrograman lain seperti C atau Java.
* Variabel dapat menyimpan nilai data dengan tipe yang berbeda-beda, seperti integer, float, string, dan lain-lain.

### Contoh Penggunaan Variabel

```python
# Menyimpan nilai berat seseorang sebagai variabel "berat"
berat = 78.7

# Menyimpan nama dan berat seseorang sebagai variabel "manusia" dengan tipe data tuple
manusia = ('David', 78.7)
```

### Penjelasan Kode

* Pada kode di atas, variabel "berat" dibuat dan nilai 78.7 disimpan ke dalam variabel tersebut.
* Pada variabel "manusia", nilai ('David', 78.7) disimpan dengan tipe data tuple.
* Tanda `=` pada kode di atas bukan berarti sama, tetapi menyimpan nilai di sebelah kanan dengan nama variabel di sebelah kiri. Operator ini `=` biasanya disebut assignment operator.


<br><br><br><br>

# Deklarasi Variabel
#### Pengenalan

Identifier adalah nama yang diberikan untuk sebuah entitas seperti class, function, variabel, dan sejenisnya. Ini membantu kita untuk membedakan satu entitas dengan entitas lainnya.

### Aturan-aturan dalam Pembuatan Variabel

* Identifier dapat berupa kombinasi huruf atau angka atau garis bawah (_), tetapi tidak dapat terdiri dari simbol khusus apa pun.
* Identifier tidak dapat dimulai dengan angka.
* Identifier tidak boleh berisi spasi atau tab.
* Identifier peka terhadap huruf besar dan kecil. Oleh karena itu, variabel `index` dan `INDEX` adalah variabel yang berbeda.
* Identifier tidak dapat menggunakan salah satu dari *Python Reserved Words*.

### Contoh Penggunaan Identifier

```python
# Identifier untuk membedakan lebar persegi panjang dari data lain
lebar = 10

# Identifier untuk membedakan tinggi persegi panjang dari data lain
tinggi = 5

# Menggunakan identifier untuk menghitung luas persegi panjang
luas_kotak = lebar * tinggi

# Mencetak hasil
print('luas area kotak = ', luas_kotak)
```

Output:
```
luas area kotak = 50
```

### Python Banned Keywords

Berikut adalah daftar kata kunci bawaan Python yang tidak dapat digunakan sebagai identifier (2024):

* `False`
* `await`
* `else`
* `import`
* `pass`
* `None`
* `break`
* `except`
* `in`
* `raise`
* `True`
* `class`
* `finally`
* `is`
* `return`
* `and`
* `continue`
* `for`
* `lambda`
* `try`
* `as`
* `def`
* `from`
* `nonlocal`
* `while`
* `assert`
* `del`
* `global`
* `not`
* `with`
* `async`
* `elif`
* `if`
* `or`
* `yield`

#### Contoh

```python
# Error: menggunakan kata kunci 'class' sebagai identifier
class = 10

# Error: menggunakan kata kunci 'def' sebagai identifier
def = 20

# Error: menggunakan kata kunci 'if' sebagai identifier
if = 30
```

Jika kita menggunakan salah satu dari kata kunci tersebut maka akan muncul *SytaxError.*

<br><br><br><br>

# Compound Assignment Operators
#### Pengenalan

Compound assignment operators adalah operator yang digunakan untuk melakukan operasi binary pada kedua operan dan menyimpan hasil operasi tersebut di operan kiri. Operator ini terdiri dari binary operator dan simple assignment operator.

#### Contoh Compound Assignment Operators

Berikut adalah contoh-contoh dari compound assignment operators:

* `+=` (penjumlahan)
* `-=` (pengurangan)
* `*=` (perkalian)
* `/=` (pembagian)
* `**=` (pangkat)
* `//=` (pembagian bulat)
* `%=` (modulus)
* `&=` (bitwise AND)
* `^=` (bitwise XOR)
* `|=` (bitwise OR)
* `<<=` (shift kiri)
* `>>=` (shift kanan)

#### Contoh Penggunaan Compound Assignment Operators

```python
# Contoh penggunaan compound assignment operators
num = 200
num += 100  # num = num + 100
print(num)  # Output: 300

num -= 100  # num = num - 100
print(num)  # Output: 200

num *= 20  # num = num * 20
print(num)  # Output: 4000

num /= 2  # num = num / 2
print(num)  # Output: 2000.0
```
<br><br><br><br>

# Input Function
#### Pengenalan

Input function `input()` merupakan sebuah fungsi bawaan dari Python untuk mendapatkan input data dari user. Fungsi ini dapat digunakan untuk memasukkan berbagai jenis data, termasuk string, integer, dan lain-lain.

#### Contoh Penerapan Input Function

```python
# Contoh penerapan input function
nama = input("Masukkan nama Anda: ")
print("Hello, " + nama)
```

Output:
```
Masukkan nama Anda: David
Hello, David
```

#### Input to Integers

Fungsi `input()` dapat digunakan untuk memasukkan bilangan bulat. Namun, fungsi `input()` selalu mengembalikan input dalam bentuk string. Untuk mengubah string menjadi bilangan bulat, nilai kembalian dari fungsi `input()` harus dikonversikan menggunakan fungsi bawaan Python lainnya yaitu `int()`.

```python
# Contoh input to integers
x = int(input("Masukkan integer pertama: "))
y = int(input("Masukkan integer kedua: "))
s = x + y
print("Total dari", x, "dan", y, "adalah", s)
```

Output:
```
Masukkan integer pertama: 1
Masukkan integer kedua: 2
Total dari 1 dan 2 adalah 3
```
<br><br><br><br>







