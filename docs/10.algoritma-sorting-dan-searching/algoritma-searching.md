---
sidebar_position: 2
---

# 10.2 Algoritma Searching


1.  Linear Search / Sequential Search
    

Linear search adalah algoritma pencarian yang sederhana dan mudah diimplementasikan. Algoritma ini bekerja dengan cara memeriksa satu per satu elemen data dalam array, dimulai dari elemen pertama. Jika elemen yang dicari ditemukan, maka algoritma akan mengembalikan indeks elemen tersebut. Jika elemen yang dicari tidak ditemukan, maka algoritma akan mengembalikan nilai -1. Berikut adalah langkah-langkah algoritma linear search:

1.  Mulai dari elemen pertama array.
    
2.  Bandingkan elemen tersebut dengan elemen yang dicari.
    
3.  Jika elemen tersebut sama dengan elemen yang dicari, maka kembalikan indeks elemen tersebut.
    
4.  Jika elemen tersebut tidak sama dengan elemen yang dicari, maka lanjutkan ke elemen berikutnya.
    
5.  Ulangi langkah 2-4 hingga akhir array.
    
6.  Jika elemen yang dicari tidak ditemukan, maka kembalikan nilai -1.
    

Berikut adalah simulasi algoritma linear search:

  
```
Data awal:

[1, 2, 3, 4, 5]

  

Elemen yang dicari: 3

  

Iterasi 1:

[1, 2, 3, 4, 5]

  

Elemen pertama sama dengan elemen yang dicari,

jadi kembalikan indeks elemen tersebut, yaitu 2.

  

Hasil: 2
```
  

Pada simulasi ini, algoritma linear search memeriksa satu per satu elemen data dalam array, dimulai dari elemen pertama. Pada iterasi pertama, elemen pertama sama dengan elemen yang dicari, sehingga algoritma mengembalikan indeks elemen tersebut, yaitu 2.

  

CONTOH KODE

```
#include <iostream>

#include <conio.h>

using namespace std;

int main()

{

int i;

int n;

int cari,ketemu=0;

int A[100];

cout<<"PROGRAM SEARCHING LINIER\n";

cout<<"--------------------------"<<endl;

cout<<"Masukan Banyak Data : ";

cin>>n;

cout<<endl;

  

for (i=1;i<=n;i++)

{

cout<<"Masukan Data Ke-"<<i<<" : ";

cin>>A[i];

}

cout<<endl;

cout<<"Input Bilangan yang dicari : ";

cin>>cari;

cout<<"--------------------------"<<endl;

cout<<endl;

for(i=0;i<=n;i++)

{

if (A[i]==cari)

{

ketemu=1;

cout<<"Data Ditemukan Pada Indeks Ke-"<<i;

}

}

if (ketemu==0)

{

cout<<"Data tidak ditemukan";

}

getch();

}
```

2.  Binary Search
    

Binary search adalah algoritma pencarian yang lebih efisien daripada linear search. Algoritma ini bekerja dengan cara membagi array menjadi dua bagian, kemudian membandingkan elemen tengah dengan elemen yang dicari. Jika elemen tengah sama dengan elemen yang dicari, maka algoritma akan mengembalikan indeks elemen tersebut. Jika elemen tengah lebih besar atau lebih kecil daripada elemen yang dicari, maka algoritma akan membagi array menjadi dua bagian lagi dan melanjutkan pencarian di bagian yang sesuai. Berikut adalah langkah-langkah algoritma binary search:

1.  Periksa apakah array kosong. Jika ya, maka kembalikan nilai -1.
    
2.  Hitung indeks tengah array.
    
3.  Bandingkan elemen tengah dengan elemen yang dicari.
    
4.  Jika elemen tengah sama dengan elemen yang dicari, maka kembalikan indeks elemen tersebut.
    
5.  Jika elemen tengah lebih besar daripada elemen yang dicari, maka lakukan binary search pada bagian kiri array.
    
6.  Jika elemen tengah lebih kecil daripada elemen yang dicari, maka lakukan binary search pada bagian kanan array.
    
7.  Ulangi langkah 3-6 hingga elemen yang dicari ditemukan atau akhir array tercapai.
    
8.  Jika elemen yang dicari tidak ditemukan, maka kembalikan nilai -1.
    

Berikut adalah simulasi algoritma binary search:

  
```
Data awal:

[1, 2, 3, 4, 5]

  
  

Elemen yang dicari: 3

  
  

Iterasi 1:

[1, 2, 3, 4, 5]

  
  

Indeks tengah array adalah 2.

  
  

Elemen tengah sama dengan elemen yang dicari,

jadi kembalikan indeks elemen tersebut, yaitu 2.

  
  

Hasil: 2
```
  

Pada simulasi ini, algoritma binary search membagi array menjadi dua bagian, yaitu bagian kiri dan bagian kanan. Bagian kiri berisi elemen-elemen dengan indeks kurang dari atau sama dengan indeks tengah, sedangkan bagian kanan berisi elemen-elemen dengan indeks lebih besar dari indeks tengah.


Binary search adalah algoritma pencarian yang lebih efisien daripada linear search, terutama untuk array yang besar. Namun, binary search hanya dapat digunakan untuk array yang telah terurut. Jika array tidak terurut, maka linear search harus digunakan

  
  

CONTOH KODE

  
```
#include <iostream>

  

// Algoritma Sorting

void bubbleSort(int arr[], int n) {

for (int i = 0; i < n-1; ++i) {

for (int j = 0; j < n-i-1; ++j) {

if (arr[j] > arr[j+1]) {

// Swap

int temp = arr[j];

arr[j] = arr[j+1];

arr[j+1] = temp;

}

}

}

}

  

// Algoritma Searching

int binarySearch(int arr[], int low, int high, int target) {

while (low <= high) {

int mid = low + (high - low) / 2;

if (arr[mid] == target)

return mid;

else if (arr[mid] < target)

low = mid + 1;

else

high = mid - 1;

}

return -1; // Element not found

}

  

int main() {

// Algoritma Sorting

int arr[] = {64, 34, 25, 12, 22, 11, 90};

int n = sizeof(arr) / sizeof(arr[0]);

bubbleSort(arr, n);

  

std::cout << "Sorted array: ";

for (int i = 0; i < n; ++i)

std::cout << arr[i] << " ";

std::cout << std::endl;

  

// Algoritma Searching

int target = 34;

int result = binarySearch(arr, 0, n - 1, target);

if (result != -1)

std::cout << "Element found at index " << result << std::endl;

else

std::cout << "Element not found" << std::endl;

  

return 0;

}
```


LATIHAN PRAKTEK

-   Implementasikan algoritma sorting dan searching dalam program.
    
-   Buat program yang mengurutkan array dan mencari elemen tertentu menggunakan algoritma sorting
    

Dalam contoh ini, saya menggunakan algoritma pengurutan Bubble Sort dan pencarian Binary Search

  
```
#include <iostream>

  

// Fungsi untuk mengurutkan array menggunakan Bubble Sort

void bubbleSort(int arr[], int n) {

for (int i = 0; i < n-1; ++i) {

for (int j = 0; j < n-i-1; ++j) {

if (arr[j] > arr[j+1]) {

// Swap

int temp = arr[j];

arr[j] = arr[j+1];

arr[j+1] = temp;

}

}

}

}

  

// Fungsi untuk mencari elemen dalam array menggunakan Binary Search

int binarySearch(int arr[], int low, int high, int target) {

while (low <= high) {

int mid = low + (high - low) / 2;

if (arr[mid] == target)

return mid;

else if (arr[mid] < target)

low = mid + 1;

else

high = mid - 1;

}

return -1; // Element not found

}

  

int main() {

const int size = 7;

int numbers[size] = {64, 34, 25, 12, 22, 11, 90};

  

// Mengurutkan array menggunakan Bubble Sort

bubbleSort(numbers, size);

  

// Menampilkan array yang sudah diurutkan

std::cout << "Array setelah diurutkan: ";

for (int i = 0; i < size; ++i) {

std::cout << numbers[i] << " ";

}

std::cout << std::endl;

  

// Mencari elemen tertentu menggunakan Binary Search

int target = 22;

int result = binarySearch(numbers, 0, size - 1, target);

  

if (result != -1) {

std::cout << "Elemen " << target << " ditemukan pada indeks " << result << std::endl;

} else {

std::cout << "Elemen " << target << " tidak ditemukan dalam array." << std::endl;

}

  

return 0;

}
```