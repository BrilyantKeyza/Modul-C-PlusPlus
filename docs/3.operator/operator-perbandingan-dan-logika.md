---
sidebar_position: 2
---

# 3.2 Operator Perbandingan

    

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