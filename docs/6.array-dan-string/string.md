---
sidebar_position: 2
---

# 6.2 String


-   Penggunaan string
    
-   Operasi dasar pada string
    
```
#include <iostream>

  

int main() {

// Array

int numbers[5] = {2, 1, 3, 4, 5};

for (int i = 0; i < 5; ++i) {

std::cout << numbers[i] << " ";

}

std::cout << std::endl;

  

// String

std::string greeting = "Hello, World!";

std::cout << greeting << std::endl;

  

return 0;

}
```

  
  

### SOAL

  

Program C++ Menghitung Panjang String

  

LATIHAN PRAKTEK

  
```
#include <iostream>

#include <string>

using namespace std;

  

int main() {

//Deklarasi variabel

string kalimat;

cout<<"Program C++ Menghitung Panjang String"<<endl;

cout<<"-------------------------------------"<<endl;

cout<<endl;

//Input string

cout<<"Masukan String : ";

getline(cin,kalimat);

//Output

cout << "Panjang sring adalah : " << kalimat.length();

return 0;

}
```