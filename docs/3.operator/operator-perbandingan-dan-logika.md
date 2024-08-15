---
sidebar_position: 2
---

# 3.2 Operator Perbandingan dan Logika


a.  Operator Perbandingan
    

Operator perbandingan digunakan untuk membandingkan dua nilai atau ekspresi dan menghasilkan nilai kebenaran (`true` atau `false).


1.  “==” (Sama Dengan)
    

Operator ini digunakan untuk mengecek apakah dua nilai sama.

Contoh:
```
int angka1 = 5;

int angka2 = 5;

bool hasil = (angka1 == angka2);

cout << "Hasilnya adalah: " << boolalpha << hasil << endl;

// hasil = true
```

2.  “!=” (Tidak Sama Dengan)
    

Operator ini digunakan untuk mengecek apakah dua nilai tidak sama.

Contoh:
```
int angka1 = 5;

int angka2 = 7;

bool hasil = (angka1 != angka2); // hasil = true
```

3.  “< ” (Kurang Dari)
    

Operator ini digunakan untuk mengecek apakah nilai pertama kurang dari nilai kedua.
```
Contoh:

int angka1 = 5;

int angka2 = 7;

bool hasil = (angka1 < angka2); // hasil = true
```


4.  “>” (Lebih Besar Dari)
    

Operator ini digunakan untuk mengecek apakah nilai pertama lebih besar dari nilai kedua.

Contoh:
```
int angka1 = 8;

int angka2 = 5;

bool hasil = (angka1 > angka2); // hasil = true
```


5.  “< =” (Kurang Dari atau Sama Dengan)
    

Operator ini digunakan untuk mengecek apakah nilai pertama kurang dari atau sama dengan nilai kedua.

Contoh:
```
int angka1 = 5;

int angka2 = 5;

bool hasil = (angka1 <= angka2); // hasil = true
```

  

6.  “>=” (Lebih Besar Dari atau Sama Dengan)
    

Operator ini digunakan untuk mengecek apakah nilai pertama lebih besar dari atau sama dengan nilai kedua.

Contoh:
```
int angka1 = 7;

int angka2 = 5;

bool hasil = (angka1 >= angka2); // hasil = true
```


b.  Operator Logika
    

Operator logika digunakan untuk menggabungkan atau memodifikasi nilai kebenaran.

1.  ‘&&’ (AND)
    

Operator ini menghasilkan `true` jika kedua ekspresi bernilai `true`.

Contoh:
```
bool kondisi1 = true;

bool kondisi2 = false;

bool hasil = (kondisi1 && kondisi2);

cout << "Hasilnya adalah: " << boolalpha << hasil << endl;

// hasil = false
```

2.  `||` (OR)
    

Operator ini menghasilkan `true` jika salah satu dari dua ekspresi bernilai `true`.

Contoh:
```
bool kondisi1 = true;

bool kondisi2 = false;

bool hasil = (kondisi1 || kondisi2); // hasil = true
```

  

3.  `!` (NOT)
    

Operator ini membalikkan nilai kebenaran suatu ekspresi.
```
Contoh:

bool kondisi1 = true;

bool hasil = !kondisi1; // hasil = false
```


CONTOH KODE

  
```
#include <iostream>

  

int main() {

int a = 5, b = 3;

  

int sum = a + b;

int difference = a - b;

int product = a * b;

int quotient = a / b;

int remainder = a % b;

  

std::cout << "Sum: " << sum << std::endl;

std::cout << "Difference: " << difference << std::endl;

std::cout << "Product: " << product << std::endl;

std::cout << "Quotient: " << quotient << std::endl;

std::cout << "Remainder: " << remainder << std::endl;

  

return 0;

}
```

Operator perbandingan dan logika sering digunakan dalam struktur keputusan (if, else) dan pengontrol aliran program lainnya untuk mengambil keputusan berdasarkan kondisi tertentu.


LATIHAN

-   Buat program sederhana yang menggunakan operator-operator tersebut.
    
-   Implementasikan operator logika dalam program kontrol aliran.
    


**SOAL**

Buatlah program kalkulator sederhana yang meminta dua bilangan dari pengguna dan kemudian menampilkan hasil penjumlahan, pengurangan, perkalian, dan pembagian.

  
```
#include <iostream>

  

int main() {

double num1, num2;

  

// Input

std::cout << "Enter first number: ";

std::cin >> num1;

std::cout << "Enter second number: ";

std::cin >> num2;

  

// Operasi Aritmatika

double sum = num1 + num2;

double difference = num1 - num2;

double product = num1 * num2;

double quotient = num1 / num2;

  

// Output

std::cout << "Sum: " << sum << std::endl;

std::cout << "Difference: " << difference << std::endl;

std::cout << "Product: " << product << std::endl;

std::cout << "Quotient: " << quotient << std::endl;

  

return 0;

}
```



**SOAL**

Program kalkulator menggunakan switch case

  

CONTOH KODE

  
  
```
#include <conio.h>

#include <iostream>

#include <string>

  

using namespace std;

  

int main(){

int bil1,bil2, pil;

float hasil;

string operasi;

cout<<"PILIH OPERATOR ARITMATIKA"<<endl;

cout<<"1. Penjumlahan"<<endl;

cout<<"2. Pengurangan"<<endl;

cout<<"3. Perkalian"<<endl;

cout<<"4. Pembagian"<<endl;

cout<<"5. Modulus"<<endl;

cout<<endl;

cout<<"Masukan Pilihan : ";

cin>>pil;

cout<<"Masukan Bilangan pertama : ";

cin>>bil1;

cout<<"Masukan Bilangan kedua : ";

cin>>bil2;

switch(pil){

case 1 : hasil=bil1+bil2;

operasi='+';

break;

case 2 : hasil=bil1-bil2;

operasi='-';

break;

case 3 : hasil=bil1*bil2;

operasi='*';

break;

case 4 : hasil=bil1/bil2;

operasi='/';

break;

case 5 : hasil=bil1%bil2;

operasi='%';

break;

default :

cout<<"Salah Masukan Operator"<<endl;

}

cout<<"-----------------------------"<<endl;

cout<<" "<<bil1<<operasi<<bil2<<"="<<hasil<<endl;

cout<<"-----------------------------"<<endl;

getch();
```


**SOAL**

Ai akan membuat sebuah program yang dapat membandingkan berat dari buah-

buahan. Sebut saja buah A dan buah B . Bantulah ai membuat program

perbandingan tersebut, dimana pada program tersebut akan mengetahui apakah :

  

-   buah A lebih besar dari buah B
    
-   buah A lebih kecil dari buah B
    
-   buah A sama dengan buah B
    
-   buah A tidak sama dengan buah B
    
-   buah A lebih besar sama dengan dari buah B
    
-   buah A lebih kecil sama dengan dari buah B
    

  

KODE

  
```
#include <iostream>

using namespace std;

  

int main() {

float berat_buah_A, berat_buah_B;

  

cout << "Masukkan berat buah A: ";

cin >> berat_buah_A;

  

cout << "Masukkan berat buah B: ";

cin >> berat_buah_B;

  

if (berat_buah_A > berat_buah_B) {

cout << "Buah A lebih besar dari buah B" << endl;

} else if (berat_buah_A < berat_buah_B) {

cout << "Buah A lebih kecil dari buah B" << endl;

} else {

cout << "Buah A sama dengan buah B" << endl;

}

  

if (berat_buah_A != berat_buah_B) {

cout << "Buah A tidak sama dengan buah B" << endl;

}

  

if (berat_buah_A >= berat_buah_B) {

cout << "Buah A lebih besar sama dengan dari buah B" << endl;

}

  

if (berat_buah_A <= berat_buah_B) {

cout << "Buah A lebih kecil sama dengan dari buah B" << endl;

}

  

return 0;

}
```