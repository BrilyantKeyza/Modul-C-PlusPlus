---
sidebar_position: 2
---

# 9.2 Prosedur


-   Pengertian dan perbedaan dengan fungsi
    

Prosedur adalah blok kode yang tidak mengembalikan nilai. Prosedur biasanya digunakan untuk melakukan tugas-tugas tertentu, seperti mencetak output atau memanipulasi data.

Perbedaan utama antara fungsi dan prosedur adalah pada nilai kembalian. Fungsi mengembalikan nilai, sedangkan prosedur tidak mengembalikan nilai.

CONTOH KODE

  
```
#include <iostream>

  

// Fungsi dengan parameter dan nilai kembalian

int add(int a, int b) {

return a + b;}

  
  

// Prosedur tanpa nilai kembalian

void greet(std::string name) {

std::cout << "Hello, " << name << "!" << std::endl;

}

  

int main() {

// Menggunakan Fungsi

int result = add(5, 3);

std::cout << "Result: " << result << std::endl;

  

// Menggunakan Prosedur

greet("Alice");

  

return 0;

}
```


LATIHAN PRAKTEK

-   Implementasikan fungsi dan prosedur dalam program
    
-   Buat program untuk menghitung luas dan keliling lingkaran menggunakan fungsi
    
```
#include <iostream>

#include <cmath> // Library untuk fungsi matematika seperti M_PI

  

// Fungsi untuk menghitung luas lingkaran

double hitungLuas(double radius) {

return M_PI * radius * radius;

}

  

// Fungsi untuk menghitung keliling lingkaran

double hitungKeliling(double radius) {

return 2 * M_PI * radius;

}

  

int main() {

// Input radius dari pengguna

double radius;

std::cout << "Masukkan panjang radius lingkaran: ";

std::cin >> radius;

  

// Memanggil fungsi untuk menghitung luas dan keliling

double luas = hitungLuas(radius);

double keliling = hitungKeliling(radius);

  

// Menampilkan hasil

std::cout << "Luas lingkaran: " << luas << std::endl;

std::cout << "Keliling lingkaran: " << keliling << std::endl;

  

return 0;

}
```