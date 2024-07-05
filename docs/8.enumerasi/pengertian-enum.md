---
sidebar_position: 1
---

# 8.1 Pengertian Enum


-   Definisi dan penggunaan enumerasi
    

Enumerasi adalah tipe data terdefinisi pengguna yang digunakan untuk mewakili daftar nilai yang terbatas. Enumerasi dapat digunakan untuk membuat kode yang lebih ringkas dan mudah dibaca. Enumerasi dapat digunakan untuk mewakili berbagai hal, seperti:

1.  Status, seperti StatusPekerjaan yang dapat memiliki nilai BEKERJA, MENCARI KERJA, atau PENSIUNAN.
    
2.  Kualitas, seperti KualitasBarang yang dapat memiliki nilai BAIK, SEDANG, atau KURANG BAIK.
    
3.  Warna, seperti Warna yang dapat memiliki nilai MERAH, HIJAU, BIRU, KUNING, atau UNGU.
    

  

CONTOH KODE

  
```
#include <iostream>

  

// Enum

enum Days { Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday };

  

int main() {

// Menggunakan Enum

Days today = Wednesday;

  

std::cout << "Today is: ";

switch (today) {

case Monday:

std::cout << "Monday";

break;

case Tuesday:

std::cout << "Tuesday";

break;

case Wednesday:

std::cout << "Wednesday";

break;

case Thursday:

std::cout << "Thursday";

break;

case Friday:

std::cout << "Friday";

break;

case Saturday:

std::cout << "Saturday";

break;

case Sunday:

std::cout << "Sunday";

break;

}

  

std::cout << std::endl;

  

return 0;

}
```


LATIHAN PRAKTEK

-   Gunakan enum dalam program
    
-   Buat program untuk mengklasifikasikan hari dalam seminggu menggunakan enum
    

KODE

 
```
#include <iostream>

  

// Enum untuk hari dalam seminggu

enum Days { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };

  

int main() {

// Meminta pengguna memasukkan nomor hari (0-6)

int dayNumber;

std::cout << "Enter a number for the day (0-6): ";

std::cin >> dayNumber;

  

// Menggunakan Enum untuk mengklasifikasikan hari

Days day;

switch (dayNumber) {

case Sunday:

day = Sunday;

std::cout << "It's Sunday, a weekend day." << std::endl;

break;

case Monday:

case Tuesday:

case Wednesday:

case Thursday:

case Friday:

day = static_cast<Days>(dayNumber);

std::cout << "It's a weekday." << std::endl;

break;

case Saturday:

day = Saturday;

std::cout << "It's Saturday, a weekend day." << std::endl;

break;

default:

std::cout << "Invalid day number entered." << std::endl;

return 1; // Keluar dari program dengan status error
```