---
sidebar_position: 1
---

# 5.1 For Loop	


-   Penggunaan for loop untuk iterasi
    

  

Perulangan dalam C++ adalah cara untuk melakukan tugas yang sama berulang kali dengan mudah. Ada tiga jenis perulangan yang bisa kita gunakan: "while", "do-while", dan "for". Perulangan "while" akan terus menjalankan tugas selama kondisi tertentu terpenuhi. Perulangan "do-while" mirip dengan "while", tapi tugas akan dijalankan setidaknya sekali sebelum memeriksa kondisi. Perulangan "for" lebih kompak, di mana kita bisa menentukan kondisi, inisialisasi, dan cara pengulangan dalam satu baris. Perulangan sangat membantu dalam membuat program yang melakukan hal-hal seperti menghitung total, mencetak pola, atau mengolah data. Pastikan untuk menggunakan perulangan dengan bijak agar tidak membingungkan program kita!


**SOAL**

  

Dengan menggunakan perulangan FOR, buatlah sebuah program sederhana

dimana akan menghitung mundur dari angka 100 sampai dengan angka 1

dengan selisih 3 angka !

KODE

  
```
#include <iostream>

using namespace std;

  

int main() {

cout << "Menghitung mundur dari 100 hingga 1 dengan selisih 3 angka:" << endl;

for (int i = 100; i >= 1; i -= 3) {

cout << i << " ";

}

cout << endl;

  

return 0;

}
```