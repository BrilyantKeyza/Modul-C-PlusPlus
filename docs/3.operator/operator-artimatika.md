---
sidebar_position: 1
---

# 3.1 Operator Aritmatika


Operator aritmatika terdiri dari operator penjumlahan, pengurangan, perkalian, pembagian, dan modulo.

1.  Operator Penjumlahan (+)
    

Operator ini digunakan untuk menambahkan dua nilai atau ekspresi.

Contoh:
```
int angka1 = 5;

int angka2 = 3;

int hasilPenjumlahan = angka1 + angka2;

  

cout << "Hasil penjumlahan adalah " << hasilPenjumlahan << endl;’

  

// hasilPenjumlahan = 8

  ```

2.  Operator Pengurangan (-)
    

Operator ini digunakan untuk mengurangi dua nilai atau ekspresi.

Contoh:
```
int angka1 = 5;

int angka2 = 3;

int hasilPengurangan = angka1 - angka2;

// hasilPengurangan = 2
```
  

3.  Operator Perkalian (*)
    

Operator ini digunakan untuk mengalikan dua nilai atau ekspresi.

Contoh:
```
int angka1 = 5;

int angka2 = 3;

int hasilPerkalian = angka1 * angka2;

// hasilPerkalian = 15
```
  

4.  Operator Pembagian (/)
    

Operator ini digunakan untuk membagi dua nilai atau ekspresi.

Contoh:
```
int angka1 = 10;

int angka2 = 2;

int hasilPenjumlahan = angka1 / angka2;

// hasilPembagian= 5
```
  

5.  Operator Modulo (%)
    

Operator ini digunakan untuk mencari sisa bagi dari dua nilai atau ekspresi.

Contoh:
```
int angka1 = 8;

int angka2 = 3;

int hasilPenjumlahan = angka1 % angka2;

// hasilmodulo = 2
```

LATIHAN

-   Buat program sederhana yang menggunakan operator-operator tersebut.
    
-   Implementasikan operator logika dalam program kontrol aliran.
    


**SOAL**

Buatlah program kalkulator sederhana yang meminta dua bilangan dari pengguna dan kemudian menampilkan hasil penjumlahan, pengurangan, perkalian, dan pembagian.

  
```
#include <iostream>

using namespace std;

int main() {

double num1, num2;

  

// Input

cout << "Enter first number: ";

cin >> num1;

cout << "Enter second number: ";

cin >> num2;

  

// Operasi Aritmatika

double sum = num1 + num2;

double difference = num1 - num2;

double product = num1 * num2;

double quotient = num1 / num2;

  

// Output

cout << "Sum: " << sum << std::endl;

cout << "Difference: " << difference << std::endl;

cout << "Product: " << product << std::endl;

cout << "Quotient: " << quotient << std::endl;

  

return 0;

}
```



**SOAL**

Program kalkulator menggunakan switch case

  

CONTOH KODE

  
```

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
```

