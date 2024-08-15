---
sidebar_position: 2
---

# 4.2 Switch Case	


-   Penggunaan switch case untuk percabangan multi-kondisi
    

  
```
#include <conio.h>

#include <iostream>

  

void main()

{

int tv;

  

cout<<"*********DAFTAR CHANNEL TV***********"<<endl;

cout<<"1. RCTI"<<endl;

cout<<"2. ANTV"<<endl;

cout<<"3. TRANS TV"<<endl;

cout<<"---------------------------------------"<<endl;

  

cout<<"Masukan Channel Pilihan = ";

cin>>tv;

  

switch(tv) {

case 1 : cout<<"Chanel yang anda pilih adalah RCTI"; break;

case 2 : cout<<"Channel yang anda pilih adalah ANTV"; break;

case 3 : cout<<"Channel yang anda pilih adalah TRANS TV"; break;

  

default : cout<<"channel tidak tersedia";

}

getch();

}
```



**SOAL**

  

Buatlah sebuah program sederhana untuk menampilkan nama bulan dengan

menggunakan statement SWITCH...CASE, dengan ketentuan jika kita

menginputkan angka 1 maka akan muncul Januari, angka 2 maka Februari,

dst.

  

LATIHAN PRAKTEK

  
```
#include <iostream>

using namespace std;

  

int main() {

int angka;

  

cout << "Masukkan angka (1-12): ";

cin >> angka;

  

switch (angka) {

case 1:

cout << "Januari" << endl;

break;

case 2:

cout << "Februari" << endl;

break;

case 3:

cout << "Maret" << endl;

break;

case 4:

cout << "April" << endl;

break;

case 5:

cout << "Mei" << endl;

break;

case 6:

cout << "Juni" << endl;

break;

case 7:

cout << "Juli" << endl;

break;

case 8:

cout << "Agustus" << endl;

break;

case 9:

cout << "September" << endl;

break;

case 10:

cout << "Oktober" << endl;

break;

case 11:

cout << "November" << endl;

break;

case 12:

cout << "Desember" << endl;

break;

default:

cout << "Angka yang dimasukkan tidak valid" << endl;

}

  

return 0;

}
```