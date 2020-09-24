# Pemrograman Fundamental: String

> Mempelajari String

Jika anda berpikir String adalah salah satu tipe data primitif di Java, maka anda salah! 

## Basic String

### Membuat String

Hampir sebagian besar programmer membuat sebuah variabel/object String menggunakan cara berikut.

```java
String teks = "Salam programmer";
```

Tanda kutip-ganda (double quote) adalah string literal atau penanda sebuah data String. 

Tapi String bukan sebuah tipe data primitif, tetapi String adalah sebuah Class. Sama seperti class lainnya. Jika kita pernah membuat sebuah object dari class Scanner, begitu juga seharusnya dengan class String. Perhatikan kode program berikut!

```java
Scanner input = new Scanner(System.in);
```

Ketika kita membuat sebuah object dari class Scanner, maka kita menggunakan keyword `new` disertai dengan nama class-nya. Begitu juga dengan String, seharusnya membuat sebuah object String adalah seperti berikut.

```java
String teks = new String("Salam programmer");
```

Hanya saja Java mengkhususkan setiap kali penggunaan string literal atau tanda kutip-ganda, maka Java akan otomatis membuatkan object string yang baru.

Ketika object string telah dibuat, kita dapat menggunakan beberapa method yang  ada, contohnya:

```java
teks.length();
```

Method `length()` dapat digunakan untuk mengetahui jumlah karakter di dalam String.

### Menggabungkan String

String dapat digabungkan dengan string lainnya dan tipe data primitif lainnya. Ada banyak cara yang dapat dilakukan untuk menggabungkan string. Perhatikan kode program berikut.

```java
public class BelajarString {
    public static void main(String[] args) {

        String nama = "Affandes";
        String teks = "Hai " + nama; // Gabung string

        System.out.println(teks);

    }
}
```

Pada contoh di atas, menggabungkan string dengan object string sehingga menjadi satu string yang utuh.

Cara lain adalah dengan menggunakan method `concat()`. Perhatikan kode program berikut.

```java
public class BelajarString {
    public static void main(String[] args) {

        String nama = "Affandes";
        String teks = "Hai ";

        System.out.println( teks.concat(nama) );

    }
}
```



## Converting String to Number

String dapat diubah menjadi angka. Perhatikan kode program berikut.

```java
public class BelajarString {
    public static void main(String[] args) {

        String teks = "2020";
        int tahun = Integer.parseInt(teks);

        System.out.println( "Sekarang tahun " + tahun );
        System.out.println( "Kemarin tahun " + (tahun-1) );

    }
}
```

Object `teks` sebenarnya adalah String yang berisi teks `2020` dalam bentuk String. Dengan method `Integer.parseInt()` teks dapat diubah menjadi tipe data angka dan dapat dilakukan proses aritmatika.

Selain `int`, object String juga dapat diubah ke tipe data primitif lainnya seperti float, char dan boolean. 

## Searching and Replacing Character in String

Terkadang kita butuh untuk mengambil sebuah karakter atau sebagian teks yang ada di dalam String. Berikut adalah contoh kode program untuk melakukan pencarian karakter di dalam String.

```java
public class BelajarString {
    public static void main(String[] args) {

        String teks = "Selamat datang";
        char c = teks.charAt(8); // ambil karakter ke 8

        System.out.println( "Karakter ke 8 adalah " + c );

    }
}
```

Dengan method `charAt()` kita dapat mengambil sebuah karakter dalam bentuk `char`. Sedangkan jika kita ingin mengambil sebagian teks yang ada pada String dapat menggunakan method `substring()`. Perhatikan kode program berikut!

```java
public class BelajarString {
    public static void main(String[] args) {

        String teks = "Selamat datang";
        String subs = teks.substring(8);

        System.out.println( "Subs: " + subs );

    }
}
```

Sedangkan jika kita ingin mencari sebuah teks atau karakter di dalam String dapat menggunakan method `indexOf()` seperti pada contoh kode program berikut ini.

```java
public class BelajarString {
    public static void main(String[] args) {

        String teks = "Selamat datang";
        int posisi = teks.indexOf("d");
        String subs = teks.substring(posisi);

        System.out.println( "Subs: " + subs );

    }
}
```

Method `indexOf()` bukan hanya mencari 1 karakter, tapi dapat mencari teks yang ada di dalam sebuah String.

Selain dapat melakukan pencarian teks, kita juga dapat melakukan *replace* terhadap teks yang ada di dalam String. Perhatikan kode program berikut!

```java
public class BelajarString {
    public static void main(String[] args) {

        String teks = "Selamat datang";
        String hasil = teks.replace("datang", "pagi");

        System.out.println( "Teks: " + teks );
        System.out.println( "Hasil: " + hasil );

    }
}
```



## Comparing String

Tidak sama seperti tipe data angka, String tidak dapat dibandingkan hanya menggunakan operator perbandingan. Ada beberapa method yang dapat digunakan untuk melakukan perbandingan terhadap String.

Yang pertama adalah method `equals()` yaitu method untuk menguji apakah String satu sama dengan String kedua. Perhatikan kode program berikut!

```java
public class BelajarString {
    public static void main(String[] args) {

        String teks1 = "Selamat datang";
        String teks2 = "selamat datang";

        System.out.println( "equals: " + teks1.equals(teks2) );
        System.out.println( "equalsIgnoreCase: " + teks1.equalsIgnoreCase(teks2) );

    }
}
```

Selain equals, kita dapat menggunakan method `compareTo()` untuk menentukan apakah String pertama lebih tinggi atau lebih rendah dari String kedua. Perhatikan contoh kode program berikut ini!

```java
public class BelajarString {
    public static void main(String[] args) {

        String teks1 = "Selamat datang";
        String teks2 = "selamat datang";

        System.out.println( "compareTo: " + teks1.compareTo(teks2) );

    }
}
```

Apabila kode program di atas akan menghasilkan output seperti berikut!

```java
compareTo: -32
```

Angka negatif yang muncul pada output yang merupakan hasil dari method `compareTo()` yang menandakan bahwa `teks1` secara leksikal lebih kecil dari `teks2`.



## Tugas