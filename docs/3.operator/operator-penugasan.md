---
sidebar_position: 4
---

# 3.4 Operator Penugasan

Operator penugasan digunakan untuk menetapkan nilai ke variabel. Di bawah ini adalah beberapa jenis operator penugasan yang sering digunakan dalam C++:

1.  Penugasan Dasar (`=`)

Operator ini digunakan untuk menetapkan nilai dari sebelah kanan ke variabel di sebelah kiri.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int x = 10;  // Menetapkan nilai 10 ke variabel x
    cout << "Nilai x: " << x << endl;

    return 0;
}
```

Pada contoh ini, `x` diberi nilai `10` menggunakan operator `=`.

2.  Penugasan Penjumlahan (`+=`)

Operator ini menambahkan nilai ke variabel dan menetapkannya kembali ke variabel tersebut.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int x = 10;
    x += 5;  // Menambahkan 5 ke x, sehingga x sekarang menjadi 15
    cout << "Nilai x setelah x += 5: " << x << endl;

    return 0;
}
```

Pada contoh ini, nilai `5` ditambahkan ke `x` menggunakan operator `+=`, sehingga `x` yang awalnya `10` menjadi `15`.

3.  Penugasan Pengurangan (`-=`)

Operator ini mengurangi nilai dari variabel dan menetapkannya kembali ke variabel tersebut.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int x = 10;
    x -= 3;  // Mengurangi 3 dari x, sehingga x sekarang menjadi 7
    cout << "Nilai x setelah x -= 3: " << x << endl;

    return 0;
}
```

Pada contoh ini, nilai `3` dikurangi dari `x` menggunakan operator `-=`, sehingga `x` yang awalnya `10` menjadi `7`.

4.  Penugasan Perkalian (`*=`)

Operator ini mengalikan nilai ke variabel dan menetapkannya kembali ke variabel tersebut.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int x = 10;
    x *= 2;  // Mengalikan x dengan 2, sehingga x sekarang menjadi 20
    cout << "Nilai x setelah x *= 2: " << x << endl;

    return 0;
}
```

Pada contoh ini, `x` dikalikan dengan `2` menggunakan operator `*=`, sehingga `x` yang awalnya `10` menjadi `20`.

5. Penugasan Pembagian (`/=`)

Operator ini membagi nilai dari variabel dan menetapkannya kembali ke variabel tersebut.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int x = 10;
    x /= 2;  // Membagi x dengan 2, sehingga x sekarang menjadi 5
    cout << "Nilai x setelah x /= 2: " << x << endl;

    return 0;
}
```

Pada contoh ini, `x` dibagi dengan `2` menggunakan operator `/=`, sehingga `x` yang awalnya `10` menjadi `5`.

6. Penugasan Modulus (`%=`)

Operator ini menghitung sisa bagi dan menetapkannya kembali ke variabel tersebut.

Contoh:

```
#include <iostream>
using namespace std;

int main() {
    int x = 10;
    x %= 3;  // Menghitung sisa bagi dari x dengan 3, sehingga x sekarang menjadi 1
    cout << "Nilai x setelah x %= 3: " << x << endl;

    return 0;
}
```

Pada contoh ini, `x` dibagi dengan `3` dan sisa bagi dari operasi ini adalah `1`, yang kemudian disimpan kembali ke `x` menggunakan operator `%=`. Sehingga, nilai akhir dari `x` adalah `1`.