---
sidebar_position: 3
---

# 3.3 Operator Logika


Operator logika digunakan untuk menggabungkan atau memodifikasi nilai kebenaran.

1.  ‘&&’ (AND)
    

Operator ini menghasilkan `true` jika kedua ekspresi bernilai `true`.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc6c9uvXLQwDDX50NmT8lc1oCAGapO91oKFPrZaEbEFCFIr3EF4AZRHqHet4PwrmhXlC0AIOTcOfuR7-u385ciOD-0-d3yxtOiyxbHGMWRYX40VwbUa0BnvVfz5Dd96l9DPUhJ6VUrJwQCbP7FLcLAGM56s?key=d3s-vJLBsYtwvRvGfZhdnw)

Contoh:
```
bool kondisi1 = true;

bool kondisi2 = false;

bool hasil = (kondisi1 && kondisi2);

cout << "Hasilnya adalah: " << boolalpha << hasil << endl;

// hasil = false
```

2.  `||` (OR)
    

Operator ini menghasilkan `true` jika salah satu dari dua ekspresi bernilai `true`.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeS66-fpCuFzKFNTkVetjZAiyB90Qv1ZVkKoA_z8SXCuTiYwfGrJRUUd7Big4lwjgGCax02XZ9BuK97u6wM53m_ENJ2Cs3l93yh0gcRAd-CuSTwfE4P4wVm5V-xl1YqXc6xeRdCaO7nMdgTwdJAQ1GRhmZC?key=d3s-vJLBsYtwvRvGfZhdnw)

Contoh:
```
bool kondisi1 = true;

bool kondisi2 = false;

bool hasil = (kondisi1 || kondisi2); // hasil = true
```

  

3.  `!` (NOT)
    

Operator ini membalikkan nilai kebenaran suatu ekspresi.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdlaou3yUXBlaQsKvwRHISxykTeTCIGU_tL-TTAa86Wonev4Ahzs3nk9RatYIwAt3rk6XQPE0W44TMww1RX1MpgE54lrDIGkRkUCOgooYXa3FnpyJUjmYPg4kHaY0cAtl6_TvtS06gMO-n7cuGk4zwzIqEZ?key=d3s-vJLBsYtwvRvGfZhdnw)
```
Contoh:

bool kondisi1 = true;

bool hasil = !kondisi1; // hasil = false
```


CONTOH KODE

  
```
#include <iostream>

  

int main() {

int a = 5, b = 3;

  

int sum = a + b;

int difference = a - b;

int product = a * b;

int quotient = a / b;

int remainder = a % b;

  

std::cout << "Sum: " << sum << std::endl;

std::cout << "Difference: " << difference << std::endl;

std::cout << "Product: " << product << std::endl;

std::cout << "Quotient: " << quotient << std::endl;

std::cout << "Remainder: " << remainder << std::endl;

  

return 0;

}
```

Operator logika sering digunakan dalam struktur keputusan (if, else) dan pengontrol aliran program lainnya untuk mengambil keputusan berdasarkan kondisi tertentu.

