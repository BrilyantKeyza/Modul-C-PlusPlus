---
sidebar_position: 4
---

# 1.4 Menggunakan Visual Studio Code


Visual Studio Code adalah editor kode sumber yang ringan namun tangguh yang berjalan di desktop kamu dan tersedia untuk Windows, macOS, dan Linux. Dilengkapi dengan dukungan bawaan untuk JavaScript, TypeScript, dan Node.js serta memiliki ekosistem ekstensi yang kaya untuk bahasa dan runtime lain (seperti C++, C#, Java, Python, PHP, Go, .NET).

### Instal Extension
1.  Buka VS Code.
2.  Pilih ikon tampilan Ekstensi pada bilah Aktivitas atau gunakan pintasan keyboard ( Ctrl+Shift+X ).
3.  Cari `'C++'`.
4.  Pilih **Instal** .
![enter image description here](https://code.visualstudio.com/assets/docs/languages/cpp/cpp-extension.png)
Untuk memeriksa apakah Kamu sudah menginstalnya:
	- Buka jendela terminal VS Code baru menggunakan ( Ctrl+Shift+` )
	- Gunakan perintah berikut untuk memeriksa kompiler GCC `g++`:
	 ```
    g++ --version
    ```
    
    Atau perintah ini untuk kompiler Clang `clang`:
    
	```
    clang --version
	```
        Output akan menunjukkan versi dan detail kompiler. Jika keduanya tidak ditemukan, pastikan file yang dapat dieksekusi kompiler Kamu berada di jalur platform Kamu ( `%PATH`di Windows, `$PATH`Linux, dan macOS) sehingga ekstensi C/C++ dapat menemukannya. Jika tidak, gunakan petunjuk di bagian di bawah ini untuk menginstal kompiler.

## Instal Compiler
Jika Anda belum menginstal kompiler, Anda dapat mengikuti salah satu tutorial instalasi di bawah ini
### Instal MinGW-x64 di Windows

Untuk memahami prosesnya, mari kita instal Mingw-w64 melalui [MSYS2](https://www.msys2.org/) . Mingw-w64 adalah perangkat gratis yang populer di Windows. Perangkat ini menyediakan versi asli GCC, Mingw-w64, dan perangkat serta pustaka C++ bermanfaat lainnya yang terkini.

1.  Unduh menggunakan [**tautan langsung ini ke penginstal MinGW**](https://github.com/msys2/msys2-installer/releases/download/2023-05-26/msys2-x86_64-20230526.exe) .
    
2.  Jalankan penginstal dan ikuti langkah-langkah panduan penginstalan. Catatan, MSYS2 memerlukan Windows 8.1 64 bit atau yang lebih baru.
    
3.  Dalam wizard, pilih Folder Instalasi yang Anda inginkan. Catat direktori ini untuk nanti. Dalam kebanyakan kasus, direktori yang direkomendasikan dapat diterima. Hal yang sama berlaku saat Anda mengatur langkah pintasan menu mulai. Setelah selesai, pastikan kotak **Run MSYS2 now** dicentang dan pilih **Finish** . Jendela terminal MSYS2 kemudian akan terbuka secara otomatis.
    
4.  Di terminal ini, instal toolchain MinGW-w64 dengan menjalankan perintah berikut:
    
    ```
    pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain
    
    ```
    
5.  Terima jumlah paket default dalam `toolchain`grup dengan menekan Enter .
![enter image description here](https://code.visualstudio.com/assets/docs/languages/cpp/cpp-install-msys2-toolchain.png)
1.  Masukkan `Y`ketika diminta apakah akan melanjutkan instalasi.
    
2.  Tambahkan jalur `bin`folder MinGW-w64 Anda ke variabel lingkungan Windows `PATH`dengan menggunakan langkah-langkah berikut:
    
    1.  Pada bilah pencarian Windows, ketik **Pengaturan** untuk membuka Pengaturan Windows Anda.
    2.  Cari **Edit variabel lingkungan untuk akun Anda** .
    3.  Dalam **Variabel Pengguna** Anda , pilih `Path`variabel lalu pilih **Edit** .
    4.  Pilih **Baru** dan tambahkan folder tujuan MinGW-w64 yang Anda rekam selama proses instalasi ke dalam daftar. Jika Anda memilih langkah instalasi default, jalurnya adalah: `C:\msys64\ucrt64\bin`.
    5.  Pilih **OK** , lalu pilih **OK** lagi di jendela **Variabel Lingkungan** untuk memperbarui `PATH`variabel lingkungan. Anda harus membuka kembali semua jendela konsol agar variabel `PATH`lingkungan yang diperbarui tersedia.
3.  Periksa apakah alat MinGW-w64 Anda terinstal dengan benar dan tersedia, buka Command Prompt **baru** dan ketik:
    
	```
	gcc --version
	g++ --version
	gdb --version

	```

Anda akan melihat keluaran yang menyatakan versi GCC, g++, dan GDB yang telah Anda instal. Jika tidak demikian, pastikan entri PATH Anda cocok dengan lokasi biner Mingw-w64 tempat alat penyusun berada.


### Instal MSVC di Windows

1.  Instal [Visual Studio Code](https://code.visualstudio.com/download) .
    
2.  Instal [ekstensi C/C++ untuk VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) . Anda dapat menginstal ekstensi C/C++ dengan mencari 'c++' di tampilan Ekstensi ( Ctrl+Shift+X ).
![enter image description here](https://code.visualstudio.com/assets/docs/cpp/cpp/cpp-extension.png)

3. Instal perangkat kompiler Microsoft Visual C++ (MSVC).

	Jika Anda memiliki Visual Studio versi terbaru, buka Visual Studio Installer dari menu Start Windows dan verifikasi bahwa beban kerja C++ telah dicentang. Jika belum terinstal, centang kotak dan pilih tombol **Modify** di installer.

	Anda juga dapat menginstal **pengembangan Desktop dengan beban kerja C++** tanpa instalasi IDE Visual Studio secara penuh. Dari halaman [Unduhan](https://visualstudio.microsoft.com/downloads/#remote-tools-for-visual-studio-2022) Visual Studio , gulir ke bawah hingga Anda melihat **Alat untuk Visual Studio** di bawah bagian **Semua Unduhan** dan pilih unduhan untuk **Alat Bangun untuk Visual Studio 2022** .
![enter image description here](https://code.visualstudio.com/assets/docs/cpp/msvc/build-tools-for-vs-2022.png)
Ini akan meluncurkan Visual Studio Installer, yang akan memunculkan dialog yang menunjukkan beban kerja Visual Studio Build Tools yang tersedia. Centang beban kerja **Desktop development with C++** dan pilih **Install** .
![enter image description here](https://code.visualstudio.com/assets/docs/cpp/msvc/desktop_development_with_cpp-2022.png)
#### Periksa instalasi Microsoft Visual C++ Anda

Untuk menggunakan MSVC dari baris perintah atau VS Code, Anda harus menjalankannya dari **Developer Command Prompt untuk Visual Studio** . Shell biasa seperti PowerShell, Bash, atau command prompt Windows tidak memiliki variabel lingkungan jalur yang diperlukan.

Untuk membuka Developer Command Prompt untuk VS, mulailah mengetik 'developer' di menu Start Windows, dan Anda akan melihatnya muncul di daftar saran. Nama persisnya bergantung pada versi Visual Studio atau Visual Studio Build Tools yang telah Anda instal. Pilih item tersebut untuk membuka prompt.

![enter image description here](https://code.visualstudio.com/assets/docs/cpp/msvc/developer-cmd-prompt-menu.png)

Anda dapat menguji apakah Anda telah menginstal kompiler C++ `cl.exe`dengan benar dengan mengetik 'cl' dan Anda akan melihat pesan hak cipta dengan versi dan deskripsi penggunaan dasar.

![enter image description here](https://code.visualstudio.com/assets/docs/cpp/msvc/check-cl-exe.png)
Jika Prompt Perintah Pengembang menggunakan lokasi BuildTools sebagai direktori awal (Anda tidak ingin meletakkan proyek di sana), navigasikan ke folder pengguna Anda ( `C:\users\{your username}\`) sebelum Anda mulai membuat proyek baru.


### Instal CGG di Linux

1.  Instal [Visual Studio Code](https://code.visualstudio.com/download) .
    
2.  Instal [ekstensi C/C++ untuk VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) . Anda dapat menginstal ekstensi C/C++ dengan mencari 'c++' di tampilan Ekstensi ( Ctrl+Shift+X ).
![enter image description here](https://code.visualstudio.com/assets/docs/cpp/cpp/cpp-extension.png)

#### Pastikan GCC terinstal

Meskipun Anda akan menggunakan VS Code untuk mengedit kode sumber, Anda akan mengompilasi kode sumber di Linux menggunakan kompiler g++. Anda juga akan menggunakan GDB untuk melakukan debug. Alat-alat ini tidak terinstal secara default di Ubuntu, jadi Anda harus menginstalnya. Untungnya, itu mudah.

Pertama, periksa apakah GCC sudah terpasang. Untuk memverifikasi apakah sudah terpasang, buka jendela Terminal dan masukkan perintah berikut:

```
gcc -v

```

Jika GCC tidak terpasang, jalankan perintah berikut dari jendela terminal untuk memperbarui daftar paket Ubuntu. Distribusi Linux yang sudah ketinggalan zaman terkadang dapat mengganggu upaya untuk memasang paket baru.

```
sudo apt-get update

```

Selanjutnya instal alat kompiler GNU dan debugger GDB dengan perintah ini:

```
sudo apt-get install build-essential gdb
```

Welcome file
Welcome file


### Instal Clang di Linux

1.  Instal [Visual Studio Code](https://code.visualstudio.com/download) .
    
2.  Instal [ekstensi C/C++ untuk VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) . Anda dapat menginstal ekstensi C/C++ dengan mencari 'c++' di tampilan Ekstensi ( Ctrl+Shift+X ).
![enter image description here](https://code.visualstudio.com/assets/docs/cpp/cpp/cpp-extension.png)


#### Pastikan Clang terinstal

Clang mungkin sudah terinstal di Mac Anda. Untuk memverifikasinya, buka jendela Terminal macOS dan masukkan perintah berikut:

```
clang --version

```

Jika Clang tidak terinstal, masukkan perintah berikut untuk menginstal alat pengembang baris perintah, yang mencakup Clang:

```
xcode-select --instal
```


## Membuat Aplikasi Hello World
Untuk memastikan compiler terinstal dan dikonfigurasi dengan benar, mari buat program C++ Hello World.

#### Membuat file C++

1.  Pada Windows, luncurkan prompt perintah Windows (Ketik **prompt perintah Windows** di bilah pencarian Windows). Pada macOS dan Linux, Anda dapat memasukkan perintah ini di terminal.
2.  Jalankan perintah berikut. Perintah tersebut akan membuat folder kosong bernama `projects`tempat Anda dapat meletakkan semua proyek VS Code Anda. Perintah berikutnya akan membuat dan mengarahkan Anda ke subfolder bernama `helloworld`. Dari sana, Anda akan membuka `helloworld`langsung di VS Code menggunakan `code`perintah tersebut.

```
mkdir projects
cd projects
mkdir helloworld
cd helloworld
code .
```
Sekarang buat file baru `helloworld.cpp`dengan nama tombol **File Baru** di File Explorer atau perintah **File** > **File Baru** .
![enter image description here](https://code.visualstudio.com/assets/docs/languages/cpp/new-file.png)

#### Tambahkan kode Hello World

Tempelkan kode berikut:

```
#include <iostream>

int main()
{
    std::cout << "Hello World" << std::endl;
}

```

Sekarang tekan Ctrl+S untuk menyimpan berkas. Anda juga dapat mengaktifkan SimpanOtomatis untuk menyimpan perubahan berkas secara otomatis, dengan mencentang **SimpanOtomatis** di menu utama **Berkas** .

#### Jalankan helloworld.cpp

1.  Pastikan Anda telah `helloworld.cpp`membukanya sehingga menjadi file aktif di editor Anda.
    
2.  Tekan tombol putar di sudut kanan atas editor.
![enter image description here](https://code.visualstudio.com/assets/docs/languages/cpp/run-play-button.png)
3. Pilih **C/C++: g++.exe build and debug file aktif** dari daftar kompiler yang terdeteksi pada sistem Anda.
![enter image description here](https://code.visualstudio.com/assets/docs/languages/cpp/select-gcc-compiler.png)
Anda hanya diminta untuk memilih compiler saat pertama kali menjalankan `helloworld.cpp`. Compiler ini menjadi compiler "default" yang ditetapkan dalam `tasks.json`berkas Anda.
4. Setelah pembangunan berhasil, Anda akan melihat "Hello World" muncul di **Terminal** terintegrasi .
![enter image description here](https://code.visualstudio.com/assets/docs/languages/cpp/helloworld-terminal-output.png)
Selamat! Anda baru saja menjalankan program C++ pertama Anda di VS Code!
