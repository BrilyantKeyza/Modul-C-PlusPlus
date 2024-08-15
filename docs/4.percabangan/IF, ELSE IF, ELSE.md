---
sidebar_position: 1
---

# 4.1 IF, ELSE IF, ELSE


-   Struktur dasar percabangan.
    

  

Percabangan dalam C++ adalah cara untuk membuat program mengambil keputusan berdasarkan kondisi tertentu. Ketika kita ingin program melakukan tugas berbeda tergantung pada nilai variabel atau kondisi tertentu, kita dapat menggunakan percabangan. Dalam C++, terdapat beberapa jenis percabangan, di antaranya adalah "if-else" dan "switch-case". Dengan menggunakan percabangan, kita bisa memberi instruksi pada program untuk menjalankan bagian kode yang berbeda tergantung pada kondisi yang terpenuhi. Misalnya, kita bisa membuat program yang memberikan pesan berbeda jika suhu di luar dingin atau panas. Percabangan ini membantu program kita untuk menjadi lebih pintar dan lebih adaptif terhadap berbagai situasi yang mungkin terjadi.

  

-   Penggunaan operator logika dalam percabangan.
    

  
```
#include <iostream>

#include <conio.h>

#include <string>

using namespace std;

  

int main()

{

string kata;

cout<<"Masukan kata = HALO"<<endl;

cin>>kata;

if (kata=="HALO"){

cout<<"Kata yang dimasukan sesuai"<<endl;

}else {

cout<<"Kata yang dimasukan tidak sesuai"<<endl;

}

  

getch();

}
```


LATIHAN PRAKTEK

-   Implementasikan beberapa percabangan dalam program.
    
-   Buat program penilaian sederhana dengan menggunakan percabangan if-else.
    


**SOAL**

Buatlah program sederhana yang meminta pengguna memasukkan angka dan menampilkan apakah angka tersebut positif, negatif, atau nol.

  

KODE

  
```
#include <iostream>

  

int main() {

int num;

  

// Input

std::cout << "Enter a number: ";

std::cin >> num;

  

// Percabangan

if (num > 0) {

std::cout << "The number is positive." << std::endl;

} else if (num < 0) {

std::cout << "The number is negative." << std::endl;

} else {

std::cout << "The number is zero." << std::endl;

}

  

return 0;

}
```



**SOAL**

Buatlah program sederhana menggunakan percabangan untuk menghitung hasil dari operasi aritmatika berdasarkan pilihan pengguna. Program ini harus dapat menangani penjumlahan, pengurangan, perkalian, dan pembagian.

  

KODE

  
  
```
#include <iostream>

using namespace std;

  

int main() {

char operasi;

float angka1, angka2;

  

cout << "Pilih operasi aritmatika (+, -, *, /): ";

cin >> operasi;

  

cout << "Masukkan dua angka: ";

cin >> angka1 >> angka2;

  

switch (operasi) {

case '+':

cout << "Hasil penjumlahan: " << angka1 + angka2 << endl;

break;

case '-':

cout << "Hasil pengurangan: " << angka1 - angka2 << endl;

break;

case '*':

cout << "Hasil perkalian: " << angka1 * angka2 << endl;

break;

case '/':

if (angka2 != 0) {

cout << "Hasil pembagian: " << angka1 / angka2 << endl;

} else {

cout << "Error: Tidak dapat melakukan pembagian dengan nol" << endl;

}

break;

default:

cout << "Operasi yang dimasukkan tidak valid" << endl;

}

  

return 0;

}
```



**SOAL**

Buatlah sebuah program sederhana untuk melakukan pengecekan nilai dengan

menggunakan statement IF..ELSE, dengan ketentuan :

-   Jika nilai 90 – 100 akan muncul predikat A
    
-   Jika nilai 80 – 89 akan muncul predikat B
    
-   Jika nilai 70 – 79 akan muncul predikat A
    
-   Jika nilai 60 – 69 akan muncul predikat D
    
-   Jika nilai 50 – 59 akan muncul predikat E
    
-   Jika nilai < 50 akan muncul Anda Tidak Lulus
    

KODE
```
#include <iostream>

using namespace std;

  

int main() {

int nilai;

  

cout << "Masukkan nilai Anda: ";

cin >> nilai;

  

if (nilai >= 90 && nilai <= 100) {

cout << "Predikat: A" << endl;

} else if (nilai >= 80 && nilai <= 89) {

cout << "Predikat: B" << endl;

} else if (nilai >= 70 && nilai <= 79) {

cout << "Predikat: C" << endl;

} else if (nilai >= 60 && nilai <= 69) {

cout << "Predikat: D" << endl;

} else if (nilai >= 50 && nilai <= 59) {

cout << "Predikat: E" << endl;

} else {

cout << "Anda Tidak Lulus" << endl;

}

  

return 0;

}
```