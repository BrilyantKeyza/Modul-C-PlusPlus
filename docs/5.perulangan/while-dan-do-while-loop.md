---
sidebar_position: 2
---

# 5.2 While dan Do-While Loop	


-   Penggunaan while dan do-while loop
    

KODE
```
#include <iostream>

  

int main() {

// For Loop

for (int i = 1; i <= 5; ++i) {

std::cout << i << " ";

}

std::cout << std::endl;

  

// While Loop

int j = 1;

while (j <= 5) {

std::cout << j << " ";

++j;

}

std::cout << std::endl;

  

// Do-While Loop

int k = 1;

do {

std::cout << k << " ";

++k;

} while (k <= 5);

std::cout << std::endl;

  

return 0;

}
```
  

LATIHAN PRAKTEK

-   Buat program yang menggunakan berbagai jenis perulangan.
    
-   Implementasikan perulangan untuk membuat pola bintang sederhana.
    

### SOAL

Buatlah program yang meminta pengguna memasukkan bilangan bulat positif N, lalu tampilkan semua bilangan ganjil dari 1 hingga N.

  
```
int main() {

int N;

  

// Input

std::cout << "Enter a positive integer N: ";

std::cin >> N;

  

// Perulangan

std::cout << "Odd numbers from 1 to " << N << ": ";

for (int i = 1; i <= N; i += 2) {

std::cout << i << " ";

}

std::cout << std::endl;

  

return 0;

}
```


### SOAL

  

Dengan menggunakan perulangan WHILE, buatlah sebuah program

sederhana dimana pengguna dapat mengisikan data berupa angka sebanyak

4 kali , dan akan menghasilkan jumlah total angka yang diinputkan.

  

KODE

  
```
#include <iostream>

using namespace std;

  

int main() {

int total = 0;

int counter = 0;

int angka;

  

cout << "Masukkan angka sebanyak 4 kali: " << endl;

while (counter < 4) {

cout << "Masukkan angka ke-" << counter + 1 << ": ";

cin >> angka;

total += angka;

counter++;

}

  

cout << "Total angka yang diinputkan: " << total << endl;

  

return 0;

}
```