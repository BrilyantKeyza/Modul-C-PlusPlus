---
sidebar_position: 1
---

# 4.1 IF, ELSE IF, ELSE


-   Struktur dasar percabangan.
    

Percabangan dalam C++ adalah cara untuk membuat program mengambil keputusan berdasarkan kondisi tertentu. Ketika kita ingin program melakukan tugas berbeda tergantung pada nilai variabel atau kondisi tertentu, kita dapat menggunakan percabangan. Dalam C++, terdapat beberapa jenis percabangan, di antaranya adalah "if-else" dan "switch-case". Dengan menggunakan percabangan, kita bisa memberi instruksi pada program untuk menjalankan bagian kode yang berbeda tergantung pada kondisi yang terpenuhi. Misalnya, kita bisa membuat program yang memberikan pesan berbeda jika suhu di luar dingin atau panas. Percabangan ini membantu program kita untuk menjadi lebih pintar dan lebih adaptif terhadap berbagai situasi yang mungkin terjadi.

- Struktur code if, else if, else
	- if
    
	![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcT_da162bO8uArtvypkIRf5cXBVakJBVMTTszEFdBgZu7ybWEIe8IQnJQGZZh_wd_H58Iz6Gqa-kqB1hqekkMYkJKnH94LzDMOm-c7jDZB4Mi0QnVmzR_UVilEEIUNqQXStD6OYJADP_2fYKMfszGfLjHz?key=d3s-vJLBsYtwvRvGfZhdnw)

	```
	if (condition) {
	// body of if statement
	}
	```

	- else if
    
    ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXciqFB5bqfdnhzPO4B87S93oIuaPbF2ZUV44mp702YxMIZ9fqlLD2cyv1RfyK69sl0A-9O-S2A1BEQZFNnKbGHPQcjqcALu2LZsayvGtzNnk2EWuhFyCidpsVciCKAV_9pyDiohWpp7K8O5vZNXRYR7bQuO?key=d3s-vJLBsYtwvRvGfZhdnw)

	```
	if (condition) {
	// block of code if condition is true
	}
	else {
	// block of code if condition is false
	}
	```

	- else

    ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcNDJdFxFvdl7MLT1plTqUNtAByrYKLz6V6RMzFHfKYDdKnwWxLbxyQy6ZD7XmISg1sv5XwIyl8Uzwpq_vkL_u5ZBekTjM4s5CPRYzLnOcmFGXnqrwTkqSQzypupZE3ux4GtQ3O9J08ubNUzidTUd7Bz81S?key=d3s-vJLBsYtwvRvGfZhdnw)

	```
	if (condition1) {
	// code block 1
	}
	else if (condition2){
	// code block 2
	}
	else {
	// code block 3
	}
	```


-   Penggunaan operator logika dalam percabangan.

```
#include <iostream>
#include <string>
using namespace std;

  

  
int main()

{

string kata;

cout << "Masukan kata = HALO"<<endl;

cin>>kata;


if (kata=="HALO"){

	cout << "Kata yang dimasukan sesuai"<<endl;
}
else {

	cout<<"Kata yang dimasukan tidak sesuai"<<endl;
}

  

}

```


LATIHAN PRAKTEK

-   Implementasikan beberapa percabangan dalam program.
    
-   Buat program penilaian sederhana dengan menggunakan percabangan if-else.
    


**SOAL**

Buatlah program sederhana yang meminta pengguna memasukkan angka dan menampilkan apakah angka tersebut positif, negatif, atau nol.

  

KODE

  
```

#include <iostream>
using namespace std;

  

  

int main() {

  

int num;

  

  

// Input

  

cout << "Enter a number: ";


cin >> num;


// Percabangan


	if (num > 0) {

	  cout << "The number is positive." << endl;
	} 
	else if (num < 0) {

	  cout << "The number is negative." << endl;
	} 
	else {

	  cout << "The number is zero." << endl;
	} 

return 0;

  

}

```



**SOAL**

Buatlah program sederhana menggunakan percabangan untuk menghitung hasil dari operasi aritmatika berdasarkan pilihan pengguna. Program ini harus dapat menangani penjumlahan, pengurangan, perkalian, dan pembagian.

  

KODE

  
  
```

#include <iostream>

  

using namespace std;

  

  

int main() {

  

char operasi;

  

float angka1, angka2;

  

  

cout << "Pilih operasi aritmatika (+, -, *, /): ";

  

cin >> operasi;

  

  

cout << "Masukkan dua angka: ";

  

cin >> angka1 >> angka2;

  

  

switch (operasi) {

	case '+': 
	
		cout << "Hasil penjumlahan: " << angka1 + angka2 << endl;
		
		break;

	case '-':

		cout << "Hasil pengurangan: " << angka1 - angka2 << endl;

		break;

  

	case '*':

		cout << "Hasil perkalian: " << angka1 * angka2 << endl;

		break;

	case '/':

		if (angka2 != 0) {

		cout << "Hasil pembagian: " << angka1 / angka2 << endl;
		
		}
		else {

		cout << "Error: Tidak dapat melakukan pembagian dengan nol" << endl;

		}
		
		break;

  

		default:

		cout << "Operasi yang dimasukkan tidak valid" << endl;

 
}

return 0;

}

```



**SOAL**

Buatlah sebuah program sederhana untuk melakukan pengecekan nilai dengan

menggunakan statement IF..ELSE, dengan ketentuan :

-   Jika nilai 90 – 100 akan muncul predikat A
    
-   Jika nilai 80 – 89 akan muncul predikat B
    
-   Jika nilai 70 – 79 akan muncul predikat A
    
-   Jika nilai 60 – 69 akan muncul predikat D
    
-   Jika nilai 50 – 59 akan muncul predikat E
    
-   Jika nilai < 50 akan muncul Anda Tidak Lulus
    

KODE
```

#include <iostream>

  

using namespace std;

  

  

int main() {

  

int nilai;

  

  

cout << "Masukkan nilai Anda: ";

  

cin >> nilai;

  

  

	if (nilai >= 90 && nilai <= 100) {

		cout << "Predikat: A" << endl;
		
		} 
		
	else if (nilai >= 80 && nilai <= 89) {

		cout << "Predikat: B" << endl;
		
		} 
		
	else if (nilai >= 70 && nilai <= 79) {

		cout << "Predikat: C" << endl;

		}
		
	else if (nilai >= 60 && nilai <= 69) {

		cout << "Predikat: D" << endl;
		
		} 
		
	else if (nilai >= 50 && nilai <= 59) {

		cout << "Predikat: E" << endl;

		} 
		
	else {

		cout << "Anda Tidak Lulus" << endl;
		
		}


return 0;

  

}

```