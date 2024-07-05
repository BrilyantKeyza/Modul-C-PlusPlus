---
sidebar_position: 1
---

# 10.1 Algoritma Sorting

1.  Bubble Sort
    

Bubble sort adalah algoritma sorting yang paling sederhana. Algoritma ini bekerja dengan cara membandingkan dua elemen data secara berurut, kemudian menukar posisinya jika elemen pertama lebih besar dari elemen kedua. Proses ini dilakukan secara berulang-ulang hingga semua elemen data terurut. Berikut adalah langkah-langkah algoritma bubble sort:

1.  Mulai dari elemen pertama data.
    
2.  Bandingkan elemen tersebut dengan elemen berikutnya.
    
3.  Jika elemen pertama lebih besar dari elemen berikutnya, maka tukar posisinya.
    
4.  Ulangi langkah 2 dan 3 hingga akhir data.
    

Berikut adalah simulasi algoritma bubble sort:

  
```
Data awal:

[5, 2, 1, 4, 3]

  
  

Iterasi 1:

[2, 5, 1, 4, 3]

  
  

Iterasi 2:

[1, 2, 5, 4, 3]

  
  

Iterasi 3:

[1, 2, 4, 5, 3]

  
  

Iterasi 4:

[1, 2, 3, 4, 5]

  
  

Data terurut:

[1, 2, 3, 4, 5]
```
  

  

Pada simulasi ini, algoritma bubble sort melakukan perbandingan antara setiap dua elemen data secara berurut. Jika elemen pertama lebih besar dari elemen kedua, maka tukar posisinya. Proses ini dilakukan secara berulang-ulang hingga semua elemen data terurut.

  

CONTOH KODE

  
```
#include <iostream>

#include <conio.h>

using namespace std;

int data[10], data2[10];

int n;

int tukar (int a,int b){

int t;

t=data[b];

data[b]=data[a];

data[a]=t;

}

  

int input(){

cout<<"Masukan Jumlah Data = ";

cin>>n;

  

cout<<endl;

for (int i=0;i<n;i++){

cout<<"Masukan Data Ke-"<<i+1<<" = ";

cin>>data[i];

data2[i]=data[i];

}

cout<<endl;

}

  

int tampil(){

for (int i=0;i<n;i++){

cout<<"["<<data[i]<<"] ";

}

cout<<endl;

}

  

int bubble_sort(){

for (int i=1; i<n;i++){

for (int j=n-1; j>=i;j--){

if (data[j]<data[j-1]){

tukar(j,j-1);

}

}

tampil();

}

cout<<endl;

}

  
  

int main()

{

cout<<"ALGORITMA BUBBLE SORT"<<endl;

cout<<"----------------------"<<endl;

input();

cout<<"Proses Bubble Sort"<<endl;

tampil();

bubble_sort();

getch();

}
```


2.  Selection Sort
    

Selection sort adalah algoritma sorting yang lebih efisien daripada bubble sort. Algoritma ini bekerja dengan cara mencari elemen terkecil atau terbesar dalam data, kemudian menukarnya dengan elemen pertama. Proses ini dilakukan secara berulang-ulang hingga semua elemen data terurut. Berikut adalah langkah-langkah algoritma selection sort:

1.  Mulai dari elemen pertama data.
    
2.  Cari elemen terkecil atau terbesar dalam data.
    
3.  Tukar posisi elemen tersebut dengan elemen pertama.
    
4.  Ulangi langkah 2 dan 3 hingga akhir data.
    

Berikut adalah simulasi algoritma selection sort:

  
```
Data awal:

[5, 2, 1, 4, 3]

  
  

Iterasi 1:

[1, 5, 2, 4, 3]

  
  

Iterasi 2:

[1, 2, 5, 4, 3]

  
  

Iterasi 3:

[1, 2, 3, 5, 4]

  
  

Iterasi 4:

[1, 2, 3, 4, 5]

  
  

Data terurut:

[1, 2, 3, 4, 5]
```


Pada simulasi ini, algoritma selection sort mencari elemen terkecil dalam data, kemudian menukarnya dengan elemen pertama. Proses ini dilakukan secara berulang-ulang hingga semua elemen data terurut.

  
  

CONTOH KODE

  
```
#include <iostream>

using namespace std;

int main() {

cout << "## Program C++ Mengurutkan Angka (Selection Sort) ##" << endl;

cout << "=====================================================" << endl;

cout << endl;

int i, j, n;

// Baca angka input dari user

cout << "Input jumlah element array: ";

cin >> n;

cout << endl;

int arr[n];

cout << "Input "<< n << " angka (dipisah dengan enter): ";

cout << endl;

for(i = 0; i < n; i++){

cout << "Angka ke-" << i+1 <<": ";

cin >> arr[i];

}

// Urutkan array dengan algoritma selection sort

for (i = 0; i < n - 1; i++) {

int Index = i;

for (j = i + 1; j < n; j++) {

if (arr[j] < arr[Index]) {

Index = j;

}

}

// Tukar posisi element terkecil dengan element pada indeks i

int temp = arr[i];

arr[i] = arr[Index];

arr[Index] = temp;

}

// Tampilan hasil pengurutan

cout << endl;

cout << "Array setelah diurutkan: ";

for (i = 0; i < n; i++) {

cout << arr[i] << " ";

}

cout << endl;

return 0;

}
```


3.  Insertion Sort
    

Insertion sort adalah algoritma sorting yang lebih efisien daripada bubble sort dan selection sort. Algoritma ini bekerja dengan cara menyisipkan elemen data ke dalam array yang telah terurut. Berikut adalah langkah-langkah algoritma insertion sort:

1.  Mulai dari elemen kedua data.
    
2.  Bandingkan elemen tersebut dengan elemen-elemen sebelumnya.
    
3.  Jika elemen tersebut lebih kecil dari elemen sebelumnya, maka sisipkan elemen tersebut ke dalam array pada posisi yang tepat.
    
4.  Ulangi langkah 2 dan 3 hingga akhir data.
    

Berikut adalah simulasi algoritma insertion sort:

  
```
Data awal:

[5, 2, 1, 4, 3]

  
  

Iterasi 1:

[2, 5, 1, 4, 3]

  
  

Iterasi 2:

[1, 2, 5, 4, 3]

  
  

Iterasi 3:

[1, 2, 4, 5, 3]

  
  

Iterasi 4:

[1, 2, 3, 4, 5]

  
  

Data terurut:

[1, 2, 3, 4, 5]
```


Pada simulasi ini, algoritma insertion sort mulai dari elemen kedua data. Elemen ini kemudian disisipkan ke dalam array yang telah terurut. Proses ini dilakukan secara berulang-ulang hingga semua elemen data terurut.

  

Pemilihan algoritma sorting yang tepat tergantung pada kebutuhan sistem. Jika kebutuhan sistem adalah algoritma sorting yang sederhana dan mudah diimplementasikan, maka bubble sort atau selection sort dapat digunakan. Namun, jika kebutuhan sistem adalah algoritma sorting yang lebih efisien, maka insertion sort dapat digunakan.

  

CONTOH KODE

  
```
#include <iostream>

using namespace std;

  

int main() {

cout << "## Program C++ Mengurutkan Angka (Insertion Sort) ##" << endl;

cout << "=====================================================" << endl;

cout << endl;

  

int i, j, n , key ;

  

// Baca angka input dari user

cout << "Input jumlah element array: ";

cin >> n;

cout << endl;

  

int arr[n];

cout << "Input "<< n << " angka (dipisah dengan enter): ";

cout << endl;

  

for(i = 0; i < n; i++){

cout << "Angka ke-" << i+1 <<": ";

cin >> arr[i];

}

  

// Urutkan array dengan algoritma insertion sort

for (i = 1; i < n; i++) {

key = arr[i];

j = i - 1;

  

while (j >= 0 && arr[j] > key) {

arr[j + 1] = arr[j];

j--;

}

  

arr[j + 1] = key;

}

  

// Tampilan hasil pengurutan

cout << endl;

cout << "Array setelah diurutkan: ";

for (i = 0; i < n; i++) {

cout << arr[i] << " ";

}

cout << endl;

  

return 0;

}
```