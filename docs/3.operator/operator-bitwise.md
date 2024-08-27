---
sidebar_position: 5
---

# 3.5 Operator Bitwise


Operator bitwise bekerja pada level bit dan melakukan operasi bit demi bit pada representasi biner dari angka.

1.  AND Bitwise (`&`)

Operator `&` membandingkan setiap bit dari dua operan. Jika kedua bit tersebut adalah `1`, maka hasilnya `1`. Jika salah satu atau kedua bit tersebut adalah `0`, maka hasilnya `0`.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int a = 5;  // 0101 dalam biner
    int b = 3;  // 0011 dalam biner
    int result = a & b;  // 0001 dalam biner, yaitu 1 dalam desimal

    cout << "Hasil dari a & b: " << result << endl;

    return 0;
}
```

Pada contoh ini, bitwise AND dilakukan antara `0101` dan `0011`. Hasilnya adalah `0001`, yaitu `1` dalam desimal.

2. OR Bitwise (`|`)

Operator `|` membandingkan setiap bit dari dua operan. Jika salah satu atau kedua bit tersebut adalah `1`, maka hasilnya `1`. Jika kedua bit tersebut adalah `0`, maka hasilnya `0`.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int a = 5;  // 0101 dalam biner
    int b = 3;  // 0011 dalam biner
    int result = a | b;  // 0111 dalam biner, yaitu 7 dalam desimal

    cout << "Hasil dari a | b: " << result << endl;

    return 0;
}
```

Pada contoh ini, bitwise OR dilakukan antara `0101` dan `0011`. Hasilnya adalah `0111`, yaitu `7` dalam desimal.

3.  XOR Bitwise (`^`)

Operator `^` membandingkan setiap bit dari dua operan. Jika bit tersebut berbeda, maka hasilnya `1`. Jika bit tersebut sama, maka hasilnya `0`.

Contoh:
```
#include <iostream>
using namespace std;

int main() {
    int a = 5;  // 0101 dalam biner
    int b = 3;  // 0011 dalam biner
    int result = a ^ b;  // 0110 dalam biner, yaitu 6 dalam desimal

    cout << "Hasil dari a ^ b: " << result << endl;

    return 0;
}
``` 

Pada contoh ini, bitwise XOR dilakukan antara `0101` dan `0011`. Hasilnya adalah `0110`, yaitu `6` dalam desimal.

4.  NOT Bitwise (`~`)

Operator `~` membalikkan semua bit dari operan. Bit `1` menjadi `0` dan bit `0` menjadi `1`.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int a = 5;  // 0101 dalam biner
    int result = ~a;  // 1010 dalam biner (dalam representasi dua's complement ini adalah -6)

    cout << "Hasil dari ~a: " << result << endl;

    return 0;
}
```

Pada contoh ini, bitwise NOT dilakukan pada `0101`. Hasilnya adalah `1010`, yang merupakan representasi biner dari `-6` dalam sistem dua's complement.

5. Left Shift Bitwise (`<<`)

Operator `<<` menggeser bit dari operan pertama ke kiri sebanyak jumlah bit yang ditentukan oleh operan kedua. Bit yang tergeser keluar di sebelah kiri diabaikan, dan bit baru yang masuk di sebelah kanan diisi dengan `0`.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int a = 5;  // 0101 dalam biner
    int result = a << 1;  // 1010 dalam biner, yaitu 10 dalam desimal

    cout << "Hasil dari a << 1: " << result << endl;

    return 0;
}
``` 

Pada contoh ini, bitwise left shift dilakukan pada `0101` dengan menggeser satu bit ke kiri. Hasilnya adalah `1010`, yaitu `10` dalam desimal.

6. Right Shift Bitwise (`>>`)

Operator `>>` menggeser bit dari operan pertama ke kanan sebanyak jumlah bit yang ditentukan oleh operan kedua. Bit yang tergeser keluar di sebelah kanan diabaikan, dan bit baru yang masuk di sebelah kiri diisi dengan `0` (untuk bilangan positif) atau `1` (untuk bilangan negatif).

Contoh:
```
#include <iostream>
using namespace std;

int main() {
    int a = 5;  // 0101 dalam biner
    int result = a >> 1;  // 0010 dalam biner, yaitu 2 dalam desimal

    cout << "Hasil dari a >> 1: " << result << endl;

    return 0;
}
```

Pada contoh ini, bitwise right shift dilakukan pada `0101` dengan menggeser satu bit ke kanan. Hasilnya adalah `0010`, yaitu `2` dalam desimal.