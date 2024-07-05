---
sidebar_position: 2
---

# 1.2 Instalasi dan Pengaturan Lingkungan Pengembangan

-   Cara Menginstal compiler C++ (misalnya g++, Visual C++)
    

Cara menginstal compiler C++ tergantung pada sistem operasi yang Anda gunakan. Berikut adalah panduan umum untuk menginstal compiler C++ pada beberapa sistem operasi yang umum digunakan:

1.  Menginstal g++ di Linux
    

-   Pada distribusi berbasis Debian (seperti Ubuntu), gunakan perintah berikut di terminal:
    

```bash

sudo apt-get update

sudo apt-get install g++

```

-   Pada distribusi berbasis Red Hat (seperti Fedora), gunakan perintah:
    

```bash

sudo yum install gcc-c++

```

2.  Menginstal g++ di MacOS
    

-   Jika Anda menggunakan Homebrew, gunakan perintah:
    

```bash

brew install gcc

```

3.  Menginstal Visual C++ di Windows
    

-   Untuk Visual Studio, Anda dapat mengunduh versi Community (gratis) atau versi lain dari situs web resmi Microsoft: [Visual Studio Download] (https://visualstudio.microsoft.com/visual-cpp-build-tools/)
    
-   Pilih komponen "Desktop development with C++" saat menginstal Visual Studio.
    

4.  Menginstal MinGW di Windows
    

-   MinGW (Minimalist GNU for Windows) menyediakan compiler GNU, termasuk g++. Anda dapat menggunakan manajer paket MSYS2 untuk menginstal MinGW di Windows.
    
-   Unduh dan instal MSYS2 dari situs resmi: [MSYS2](https://www.msys2.org/)
    
-   Buka MSYS2 Shell dan jalankan perintah berikut:
    

```bash

pacman -Syu

pacman -S mingw-w64-x86_64-toolchain

```

5.  Menguji Coba Instalasi
    

-   Setelah menginstal compiler, buka terminal atau command prompt dan jalankan perintah berikut untuk memastikan compiler telah terpasang dengan baik:
    

```bash

g++ --version # Untuk g++

cl # Untuk Visual C++

```

Dengan mengikuti panduan di atas, Anda seharusnya dapat menginstal compiler C++ yang sesuai dengan sistem operasi Anda. Setelah instalasi selesai, Anda dapat membuat dan menjalankan program C++ menggunakan compiler tersebut.


-   Menggunakan IDE (Integrated Development Environment)
    

Menggunakan Integrated Development Environment (IDE) membuat pengembangan perangkat lunak lebih efisien dengan menyediakan berbagai alat dan fitur yang membantu dalam menulis, menguji, dan menjalankan kode. Berikut adalah panduan umum menggunakan dua IDE populer untuk pengembangan C++:

1.  Visual Studio Code(VSCode)
    

Langkah-Langkah

1.  Instal Visual Studio Code
    

Unduh dan instal Visual Studio Code dari [situs resmi](https://code.visualstudio.com/).

2.  Instal Extension C/C++
    

-   Buka VSCode.
    
-   Pada sidebar, klik pada ikon ekstensi (ikon kubus persegi panjang).
    
-   Cari "C/C++" dan instal ekstensi yang dikembangkan oleh Microsoft.
    

3.  Buat Proyek C++ Baru
    

-   Buka terminal di VSCode (`Ctrl + backtick` atau `View > Terminal`).
    
-   Buat direktori untuk proyek dan masuk ke dalamnya:
    

```bash

mkdir nama_proyek

cd nama_proyek

```

-   Inisialisasi Proyek C++ dengan perintah:
    

```bash

g++ --version # Pastikan g++ terinstal

g++ -std=c++11 -o main main.cpp # Buat file main.cpp dan kompilasi

```

4.  Konfigurasi dan Debug
    

-   Buat file `launch.json` untuk mengonfigurasi pengaturan debug.
    
-   Tambahkan konfigurasi berikut:
    

```json

{

"version": "0.2.0",

"configurations": [

{

"name": "Debug C++",

"type": "cppdbg",

"request": "launch",

"program": "${workspaceFolder}/main",

"args": [],

"stopAtEntry": false,

"cwd": "${workspaceFolder}",

"environment": [],

"externalConsole": false,

"MIMode": "gdb",

"setupCommands": [

{

"description": "Enable pretty-printing for gdb",

"text": "-enable-pretty-printing",

"ignoreFailures": true

}

],

"preLaunchTask": "g++ build active file"

}

]

}

```

-   Pastikan ada file `tasks.json` di folder `.vscode`. Jika tidak ada, buat file tersebut dengan konfigurasi untuk membangun proyek:
    

```json

{

"version": "2.0.0",

"tasks": [

{

"label": "g++ build active file",

"type": "shell",

"command": "/usr/bin/g++",

"args": [

"-g",

"${file}",

"-o",

"${fileDirname}/${fileBasenameNoExtension}"

],

"group": {

"kind": "build",

"isDefault": true

}

}

]

}

```

5.  Mulai Debugging
    

-   Tambahkan breakpoint di dalam kode.
    
-   Pilih konfigurasi "Debug C++" di sidebar VSCode.
    
-   Tekan tombol F5 untuk mulai debugging.


2.  Visual Studio
    

Langkah-langkah

1.  Instal Visual Studio
    

Unduh dan instal Visual Studio dari [situs resmi](https://visualstudio.microsoft.com/)

2.  Pilih Beban Kerja untuk Pengembangan C++
    

Pada saat instalasi, pastikan untuk memilih beban kerja "Desktop development with C++".

3.  Buat Proyek C++ Baru
    

-   Buka Visual Studio.
    
-   Pilih "Create a new project" atau "Open a project or solution".
    
-   Pilih jenis proyek C++ yang diinginkan dan ikuti panduan untuk menyelesaikan proses pembuatan proyek.
    

5.  Menulis dan Mengkompilasi Kode
    

-   Buka atau buat file sumber C++.
    
-   Tulis kode Anda.
    
-   Klik kanan pada proyek dalam Solution Explorer dan pilih "Build" untuk mengkompilasi proyek.
    

7.  Konfigurasi dan Debug
    

-   Tambahkan breakpoint di dalam kode.
    
-   Pilih konfigurasi "Debug" dan tekan tombol F5 untuk mulai debugging.
    

Contoh Kode


```
#include <iostream>

  

int main() {

  

std::cout << "Hello, World!" << std::endl;

  

return 0;

  

}
```