---
sidebar_position: 2
---

# 2.2 Tipe Data


-   Tipe Data Dasar: int, float, double, char, bool.
    

Tipe data dasar adalah kategori utama tipe data yang digunakan untuk menyimpan nilai dalam pemrograman. Berikut adalah penjelasan singkat tentang beberapa tipe data dasar yang umum digunakan:

1.  Tipe Data int (Integer)
    

Digunakan untuk menyimpan nilai bilangan bulat (tanpa desimal).

Contoh:
```
int angka = 10;
```

  

2.  Tipe Data float
    

Digunakan untuk menyimpan nilai desimal (floating-point) dengan presisi rendah.

Contoh:
```
int float = 10.3;
```

  

3.  Tipe Data char (Character)
    

Digunakan untuk menyimpan satu karakter atau huruf.

Contoh:
```
char jenisKelamin = 'L';
```
  

4.  Tipe Data double
    

Mirip dengan `float`, tetapi menyimpan nilai desimal dengan presisi ganda.

Contoh:
```
double tinggi = 175.5;
```
  

5.  Tipe Data bool (Boolean)
    

Digunakan untuk menyimpan nilai kebenaran, yaitu `true` atau `false`.

Contoh:
```
bool isSunny = true;
```


-   Pemahaman Tentang Batas Tipe Data
    

CONTOH PENGGUNAAN VARIABEL DAN TIPE DATA
```
#include <iostream>

  

int main() {

// Tipe data int

int umur = 25;

// Tipe data float

float nilaiFloat = 3.14f; // f menandakan literal float

// Tipe data double

double tinggi = 175.5;

  

// Tipe data char

char jenisKelamin = 'L';

  

// Tipe data bool

bool isSunny = true;

  

// Menampilkan nilai variabel

std::cout << "Umur: " << umur << std::endl;

std::cout << "Nilai Float: " << nilaiFloat << std::endl;

std::cout << "Tinggi: " << tinggi << std::endl;

std::cout << "Jenis Kelamin: " << jenisKelamin << std::endl;

std::cout << "Cuaca Cerah? " << std::boolalpha << isSunny << std::endl;

  

return 0;

}
```
  

  

Pada contoh di atas, kita mendeklarasikan dan menginisialisasi variabel dengan tipe data int, float, double, char, dan bool, lalu menampilkan nilai-nilai tersebut. boolalpha digunakan untuk menampilkan nilai bool sebagai "true" atau "false" dalam output.