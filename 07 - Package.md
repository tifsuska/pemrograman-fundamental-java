# Programming Fundamentals: Package

> Quote of the day

Bayangkan kita memiliki sebuah program yang terdiri dari banyak class dan file. Akan lebih masuk akal jika class-class tersebut diorganisasikan dan dikelompokkan ke dalam folder/directory tertentu supaya lebih mudah dalam mencari dan memahami relasi antar class nya. Folder/directory tadi disebut dengan package.

## Membuat package

Misalkan kita memiliki beberapa class, yaitu:

1. Class Persegi
2. Class PersegiPanjang
3. Class Segitiga
4. Class Lingkaran
5. Class Hexagonal

Mungkin saja di dalam program kita terdapat banyak sekali class. Class-class di atas bisa saja bagian dari project yang kita buat. 

Kelima class di atas dapat kita kelompokkan ke dalam package khusus dengan nama `shape` atau `2d`. Penamaan package dapat disesuaikan dengan keinginan. Selagi nama simple dan sesuai aturan penamaan package.

Ketika ke 5 class tadi dimasukkan ke package yang sudah ditentukan, maka di dalam kode program harus ditambahkan keyword package untuk menyatakan posisi packagenya. Perhatikan kode program berikut!

```java
package com.affandes.java.2d;

public class Persegi {

    //...
    
}

```

Dengan demikian, maka kode program di atas dapat disimpan ke dalam folder `com/affandes/java/2d`. 

## Penamaan Package

Tidak ada aturan khusus dalam memberikan nama package pada project Java. Hanya saja untuk menghindari kesamaan nama package antara project kita dengan project orang lain, maka digunakan aturan-aturan tertentu, yaitu:

1. Gunakan domain di awal nama package. Domain dapat berupa alamat web atau nama unik, misalnya `com.affandes` diambil dari kebalikan alamat website `affandes.com`. 
2. Hindari penggunaan angka di awal nama package.
3. Hindari penggunaan simbol lain selain `_` (underscore).
4. Gunakan huruf kecil.

Cara paling muda membuat nama class adalah dengan menggunakan nama domain. Berikut adalah beberapa konversi nama package dari domain.

| Nama Domain      | Nama Package      |
| ---------------- | ----------------- |
| belajar-java.org | org.belajar_java  |
| 12jurus.java.com | com.java._12jurus |
| myweb.int        | int_.myweb        |

## Menggunakan Class di dalam Package

Ketika class sudah dimasukkan ke dalam sebuah package, maka ada cara khusus untuk memanggil class tersebut di dalam class lain, yaitu dengan menambahkan keyword import. Perhatikan contoh kode program berikut ini.

```java
import com.affandes.java.2d.Persegi;

public class BelajarPackage {
    public static void main(String[] args) {

        Persegi object = new Persegi();
        
        //...

    }
}
```

Keyword import di atas hanya digunakan apabila memanggil class pada package yang berbeda.

### Tutorial memahami package

Pada tutorial ini kita akan membuat beberapa class dan package, serta menggunakan class-class tersebut di dalam class lainnya.

Pertama, buatlah sebuah project. 

Project dapat berupa folder biasa saja, kemudian kita akan membuat class dan packagenya di dalam project tersebut. Perhatikan gambar berikut!

![image-20200916072931824](G:\My Drive\Works\HyNusantara\Blog\Programming Fundamental with Java\assets\image-20200916072931824.png)

Kedua, buatlah dua buah folder/direktori dengan nama **src** dan **out**. Kedua folder ini sebenarnya dapat diberi nama sesuai dengan keinginan. Silahkan sesuaikan jika nama foldernya berbeda.

![image-20200916073344160](G:\My Drive\Works\HyNusantara\Blog\Programming Fundamental with Java\assets\image-20200916073344160.png)

Ketiga, buatlah sebuah file **Main.java** di dalam folder **src** tadi. Gunakan text editor seperti Notepad (Windows) atau nano (Linux) atau IDE yang biasa digunakan. 

![image-20200916073552805](G:\My Drive\Works\HyNusantara\Blog\Programming Fundamental with Java\assets\image-20200916073552805.png)

Keempat, buatlah beberapa folder/direktori lainnya di dalam folder src tadi, kemudian buatlah beberapa file class di dalam folder yang baru. Misalnya jadi seperti ini.

![image-20200916074511971](G:\My Drive\Works\HyNusantara\Blog\Programming Fundamental with Java\assets\image-20200916074511971.png)

Berikut kode program yang ada di dalam class Salam.

```java
package baru;

public class Salam {
  
}
```

Berikut kode program yang ada di dalam class Persegi.

```java
package umum;

public class Persegi {
    
}
```



Kelima, bukalah file Main.java, kemudian salin dan perhatikan kode program berikut!

```java
public class Main {
    public static void main(String[] args) {
        Salam salam = new Salam();
        Persegi persegi = new Persegi();
    }
}
```

Jika kode program di atas dijalankan, maka akan muncul error. Ini karena kita sedang  menggunakan class Salam dan class Persegi di package/direktori yang berbeda dengan class Main. Pada kondisi seperti di atas, class Main tidak dapat secara otomatis mencari class Salam dan class Persegi yang ada di package/direktori yang berbeda, sehingga kita harus membantu class Main mencari package-nya.

Modifikasi kode program di atas menjadi seperti ini.

```java
import baru.Salam;
import umum.Persegi;

public class Main {
    public static void main(String[] args) {
        Salam salam = new Salam();
        Persegi persegi = new Persegi();
    }
}
```

Dengan menambahkan keyword import kita dapat melakukan pemanggilan terhadap class-class lain di packages yang berbeda.