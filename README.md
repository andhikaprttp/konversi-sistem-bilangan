# konversi-sistem-bilangan
---
Mata Pelajaran : Sistem Komputer
> Guru Kami      : [Pak Erwin S.kom](pakerwin.md)

Konversi sistem bilangan menggunakan bahasa C++

Terdapat 4 Sistem Bilangan pada komputer
- Desimal 
- Hexadesimal
- Biner
- Oktal

---

- Program ini meminta input dari pengguna berupa pilihan menu dan bilangan yang akan dikonversi.
- Menggunakan switch case untuk memproses pilihan menu yang dipilih pengguna.
- Untuk konversi dari desimal ke biner, oktal, dan heksadesimal, program menggunakan operasi modulus dan pembagian.
- Untuk konversi dari biner, oktal, dan heksadesimal ke desimal, program menggunakan perhitungan nilai pangkat yang sesuai dengan masing-masing sistem bilangan.

# Instalasi 📜

- Pertama Buka terminal 
- Pastikan terdapat [compiler c++](https://en.wikipedia.org/wiki/List_of_compilers) dan [git](https://git-scm.com/) pada terminal anda.

lalu ketik 

```bash
git clone https://github.com/andhikaprttp/konversi-sistem-bilangan

```
untuk mendownload program ini.

ketik
```bash
 cd konversi-sistem-bilangan
```

lalu compile file ``main.cpp`` dengan cara 
> sebagai contoh saya menggunakan clang , kemungkinan berbeda compiler berbeda juga perintah nya 

```bash
clang++ main.cpp -o main
```

perintah ``clang++`` untuk mengcompile program
perintah ``-o`` untuk mengganti nama file output dari proses compile

dan jalankan menggunakan perintah

```
./main

```



# Desimal Ke Biner 
Sistem bilangan desimal adalah sistem standar yang melambangkan bilangan bulat dan bukan bilangan bulat
sumber : [Wikipedia Indonesia](https://id.wikipedia.org/wiki/Sistem_bilangan_desimal)

Sistem bilangan biner atau sistem bilangan basis dua adalah sebuah sistem penulisan angka dengan menggunakan dua simbol yaitu 0 dan 1
sumber: [Wikipedia Indonesia](https://id.wikipedia.org/wiki/Sistem_bilangan_biner)

## Kode sumber desimal ke biner
```c++
      #include <iostream>
      using namespace std;
      int main(){
      cout << "Masukkan bilangan desimal: ";
            cin >> desimal;
            hasil = 0;
            pangkat = 0;
            while (desimal > 0) {
                sisa = desimal % 2;
                hasil += sisa * pow(10, pangkat);
                desimal /= 2;
                pangkat++;
            }
            cout << "Bilangan biner: " << hasil << endl;
            return 0;
       }

```

# 
