---
sidebar_position: 1
---

# 6.1 Array	


-   Pengertian Array
    

  

Dalam bahasa pemrograman C++, array adalah struktur data yang digunakan untuk menyimpan kumpulan elemen data yang memiliki tipe data yang sama. Elemen-elemen ini disimpan dalam memori secara berurutan dan diakses menggunakan indeks. Indeks dimulai dari 0 dan berakhir pada (jumlah elemen - 1).

  

-   Inisialisasi, akses, dan manipulasi array


LATIHAN PRAKTEK

-   Buat program yang menggunakan array dan string.
    
-   Implementasikan program untuk mencari nilai maksimum dalam array.
    

  

### SOAL

Buatlah program yang mengambil 5 nilai integer dari pengguna, menyimpannya dalam array, dan kemudian menampilkan nilai maksimum dari array tersebut.
```
#include <iostream>

  

int main() {

const int size = 5;

int numbers[size];

  

// Input

std::cout << "Enter 5 integers:" << std::endl;

for (int i = 0; i < size; ++i) {

std::cout << "Enter number " << i + 1 << ": ";

std::cin >> numbers[i];

}

  

// Mencari nilai maksimum

int max = numbers[0];

for (int i = 1; i < size; ++i) {

if (numbers[i] > max) {

max = numbers[i];

}

}

  

// Output

std::cout << "Maximum value: " << max << std::endl;

  

return 0;

}
```


### SOAL

  

Contoh jika berdasarkan array yang kita buat diatas dan kita ingin mencetaknilai 2 dan 15 maka index yang diakses adalah 0 dan 3 karena nilai 2 berada pada index ke 0 dan nilai 15 berada pada index ke-3. Lihat program berikut:

  

LATIHAN PRAKTEK

  
 ```
#include <iostream>

using namespace std;

int main() {

  

int nilai[5]={2,4,9,15,22};

cout<<nilai[0]<<endl;

cout<<nilai[3]<<endl;

return 0;

}
```


### SOAL

  

Mengakses Nilai Array dengan Perulangan

  

Untuk nilai array kebanyakan cara mengaksesnya menggunakan bantuan perulangan for. karena akses index membutuhkan deretan angka yang dapat kita buat dengan mudah menggunakan perulangan.

  

LATIHAN PRAKTEK
```
#include <iostream>

using namespace std;

int main() {

  

int nilai[5]={2,4,9,15,22};

for (int i=0;i<5;i++){

cout<<nilai[i]<<endl;

}

getch();

}
```


### SOAL

Studi Kasus sebuah nilai Contoh Program Tentang Array di C++

LATIHAN PRAKTEK
```
#include <conio.h>

#include <iostream>

#include <string>

using namespace std;

int main()

{

int n;

string nama[10],status[10];

int nilai[10];

  

cout<<"Masukan Jumlah Data = ";

cin>>n;

cout<<endl;

  

for (int i=0; i<n; i++) {

cout<<endl;

cout<<"Data ke-"<<i+1<<endl;

cout<<"Masukan Nama = ";

cin>>nama[i];

cout<<"Masukan Nilai = ";

cin>>nilai[i];

if (nilai[i]<=50) {

status[i]="Tidak Lulus";

} else {

status[i]="Lulus";

}

}

cout<<endl;

cout<<"DAFTAR NILAI MAHASISWA"<<endl;

cout<<"-------------------------------------------"<<endl;

cout<<"No Nama Nilai Status "<<endl;

cout<<"-------------------------------------------"<<endl;

  

for (int i=0; i<n;i++) {

cout<<i+1<<" "<<nama[i]<<" "<<nilai[i]<<" "<<status[i]<<endl;

cout<<"-------------------------------------------"<<endl;

}

  

getch();

}
```