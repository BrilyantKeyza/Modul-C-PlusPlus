---
sidebar_position: 1
---

# 7.1 Definisi dan Penggunaan


-   Membuat struktur data sederhana
    

Struktur adalah tipe data terdefinisi pengguna yang digunakan untuk menggabungkan beberapa tipe data dasar menjadi satu unit. Struktur dapat digunakan untuk mewakili berbagai hal, seperti:

1.  Data dari suatu objek, seperti data dari suatu buku, yaitu judul, pengarang, penerbit, dan tahun terbit.
    
2.  Data dari suatu transaksi, seperti data dari suatu pembelian, yaitu tanggal, jumlah barang, dan total harga.
    
3.  Data dari suatu permainan, seperti data dari suatu pemain, yaitu nama, usia, dan tingkat kesulitan.
    

Struktur dapat digunakan untuk membuat kode yang lebih ringkas dan mudah dibaca. Misalnya, jika kita ingin menyimpan data dari suatu buku, kita dapat menggunakan struktur sebagai berikut:

  
```
struct Buku {

std::string judul;

std::string pengarang;

std::string penerbit;

int tahun_terbit;

};
```

  

Struktur ini memiliki empat anggota, yaitu:

1.  judul: tipe data std::string untuk menyimpan judul buku.
    
2.  pengarang: tipe data std::string untuk menyimpan nama pengarang buku.
    
3.  penerbit: tipe data std::string untuk menyimpan nama penerbit buku.
    
4.  tahun_terbit: tipe data int untuk menyimpan tahun terbit buku.
    

-   Mengisi Nilai dan Mengakses Anggota struktur
    

Kita dapat menggunakan struktur ini dengan cara membuat variabel dari tipe data struktur yang telah kita definisikan. Misalnya, untuk membuat variabel buku dari tipe data Buku, kita dapat menggunakan kode berikut:

  
  
```
Buku buku;

//Kemudian, kita dapat mengisi nilai anggota struktur buku dengan kode berikut:

buku.judul = "Buku Pemrograman C++";

buku.pengarang = "Muhammad Bard";

buku.penerbit = "Penerbit Erlangga";

buku.tahun_terbit = 2023;
```


Setelah itu, kita dapat mengakses nilai anggota struktur buku dengan cara menggunakan operator titik (.). Misalnya, untuk mencetak judul buku, kita dapat menggunakan kode berikut:

  
```
std::cout << buku.judul << std::endl;
```
  

Struktur adalah tipe data terdefinisi pengguna yang digunakan untuk menggabungkan beberapa tipe data dasar menjadi satu unit. Struktur dapat digunakan untuk membuat kode yang lebih ringkas dan mudah dibaca.

  
  

CONTOH KODE
```
#include <iostream>

  

// Struct

struct Person {

std::string name;

int age;

};

  

int main() {

// Menggunakan Struct

Person person1;

person1.name = "John";

person1.age = 30;

  

std::cout << "Name: " << person1.name << std::endl;

std::cout << "Age: " << person1.age << std::endl;

  

return 0;

}
```


LATIHAN PRAKTEK

-   Implementasikam struct dalam program
    
-   Buat program manajemen data mahasiswa dengan menggunakan struktur
    

KODE
```
#include <iostream>

#include <iomanip>

#include <vector>

  

// Struktur untuk data mahasiswa

struct Mahasiswa {

std::string nama;

int nim;

double ipk;

};

  

// Fungsi untuk menampilkan data mahasiswa

void tampilkanData(const Mahasiswa& mahasiswa) {

std::cout << "NIM: " << std::setw(8) << mahasiswa.nim;

std::cout << "Nama: " << std::setw(20) << mahasiswa.nama;

std::cout << "IPK: " << std::setw(4) << std::fixed << std::setprecision(2) << mahasiswa.ipk << std::endl;

}

  

int main() {

// Membuat vector untuk menyimpan data mahasiswa

std::vector<Mahasiswa> daftarMahasiswa;

  

// Menambahkan beberapa data mahasiswa ke dalam vector

daftarMahasiswa.push_back({"John Doe", 123456, 3.75});

daftarMahasiswa.push_back({"Jane Smith", 234567, 3.90});

daftarMahasiswa.push_back({"Bob Johnson", 345678, 3.60});

  

// Menampilkan data mahasiswa

std::cout << "Daftar Mahasiswa:\n";

std::cout << std::setw(15) << "NIM" << std::setw(25) << "Nama" << std::setw(10) << "IPK" << std::endl;

std::cout << "--------------------------------------\n";

for (const Mahasiswa& mhs : daftarMahasiswa) {

tampilkanData(mhs);

}

  

return 0;

}
```