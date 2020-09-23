# Programming Fundamentals: Basic Input dan Output

> Quote of the day

Semua program membutuhkan input dan menghasilkan output. Pada bab ini akan dibahas tentang fundamental dari input dan output pada Java.

## Input Scanner

Cara paling sederhana untuk mengambil input dari keyboard adalah dengan menggunakan Scanner. Perhatikan contoh kode program berikut ini!

```java
import java.util.Scanner;

public class BelajarScanner {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        String nama = input.nextLine();
        System.out.println( "Hai " + nama );

    }
}
```

Kode program di atas ketika dijalankan akan tidak menampilkan tampilan apa-apa. Tetapi ketika kita memasukkan inputan menggunakan keyboard, maka program tadi akan menerima input dari user. Tekan `enter` maka kode program berikutnya akan menampilkan tulisan `Hai <nama_yg_diinput>` pada layar konsol.

Bagian `<nama_yg_diinput>` akan sesuai dengan apa yang kita inputkan sebelumnya menggunakan keyboard. Dengan demikian kita sudah berhasil mengambil input dari keyboard.

Namun, program sebelumnya tidak terlihat baik. Untuk itu kita perlu modifikasi kode program tadi menjadi seperti ini.

```java
import java.util.Scanner;

public class Simpel {
    public static void main(String[] args) {

        System.out.print("Nama = ");
        Scanner input = new Scanner(System.in);
        String nama = input.nextLine();
        System.out.println( "Hai " + nama );

    }
}
```

Dengan demikian kita dapat tampilan aplikasi yang lebih baik.

### Import java.util.Scanner

Perlu kita perhatikan ketika menggunakan Scanner, kita perlu menambahkan baris `import java.util.Scanner;` pada kode program kita seperti contoh di atas. Gunanya adalah untuk memastikan kita dapat menggunakan class Scanner yang ada pada package yang berbeda, yaitu package `java.util`.

Apabila kita tidak menambahkan baris `import java.util.Scanner` bisa dipastikan kode program tadi tidak akan jalan sama sekali.

### Import java.util.*

Kita juga bisa menggunakan `import java.util.*` untuk menggunakan class Scanner, tidak ada perbedaan sama sekali dari hasil program yang dijalankan.

Penggunaan baris `import java.util.*` berarti kita akan menggunakan semua class yang ada di dalam package `java.util`, sedangkan penggunaan baris `import java.util.Scanner` berarti kita hanya akan menggunakan class Scanner yang ada di dalam package `java.util`.

Perhatikan contoh kode program berikut ini!

```java
import java.util.*;

public class Simpel {
    public static void main(String[] args) {

        System.out.print("Nama = ");
        Scanner input = new Scanner(System.in);
        String nama = input.nextLine();
        System.out.println( "Hai " + nama );
        
    }
}
```

Hasil yang diperoleh akan sama saja dengan kode program sebelumnya.

### Input data angka

Pada dasarnya, Scanner dapat membaca semua karakter yang  diinputkan melalui keyboard. Namun, untuk mengambil data angka, class Scanner memiliki method khusus, salah satunya adalah `nextInt()`. Perhatikan kode program berikut!

```java
import java.util.Scanner;

public class Umur {
    public static void main(String[] args) {

        System.out.print("Tahun lahir = ");
        Scanner input = new Scanner(System.in);
        
        int tahun = input.nextInt();
        int umur = 2020 - tahun;
        System.out.println( "Umur = " + umur );

    }
}
```

Selain menghasilkan `int`, Scanner juga dapat menghasilkan tipe data lainnya, seperti pada tabel berikut!

| No   | Tipe data | Method                 |
| ---- | --------- | ---------------------- |
| 1    | String    | next() atau nextLine() |
| 2    | int       | nextInt()              |
| 3    | double    | nextDouble()           |
| 4    | boolean   | nextBoolean()          |

Perhatikan contoh kode program berikut!

```java
import java.util.Scanner;

public class InScanner {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        System.out.print("Nama = ");
        String nama = input.nextLine();

        System.out.print("Tahun lahir = ");
        int tahun = input.nextInt();

        int umur = 2020 - tahun;
        System.out.printf("%s (%d tahun)", nama, umur);
        
    }
}
```

Ketika membuat input menggunakan Scanner, kita dapat mengambil berbagai macam tipe data sekaligus sesuai dengan kebutuhan. 

## Input Buffered Reader

Sama halnya dengan Scanner, BufferedReader dapat digunakan untuk mengambil data input dari keyboard. Perhatikan kode program berikut!

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Buffered {
    public static void main(String[] args) {

        BufferedReader input = new BufferedReader(new InputStreamReader(System.in));

        try {
            System.out.print("Nama = ");
            String nama = input.readLine();
            System.out.println( "Hai " + nama );
        } catch (IOException exception) {
            System.out.println("Error input!");
        }

    }
}
```

Jika kode program di atas dijalankan, maka hasilnya sama dengan kode program sebelumnya.

### Import yang banyak

Jika kita menggunakan BufferedReader, kita harus menggunakan beberapa `import` agar kode program dapat dijalankan. Ketiga baris import itu harus dibuat, jika tidak akan menghasilkan error.

### Gunakan import java.io.*

Kita dapat mempermudah baris import sebelumnya dengan menggunakan baris `import java.io.*`. Cara ini lebih mudah digunakan, sedangkan hasilnya tetap sama. Perhatikan kode program berikut!

```java
import java.io.*;

public class Buffered {
    public static void main(String[] args) {

        BufferedReader input = new BufferedReader(new InputStreamReader(System.in));

        try {
            System.out.print("Nama = ");
            String nama = input.readLine();
            System.out.println( "Hai " + nama );
        } catch (IOException exception) {
            System.out.println("Error input!");
        }

    }
}
```

### Input data angka

Berbeda dengan Scanner, class BufferedReader tidak memiliki method khusus untuk mengambil data angka. Sehingga kita harus menggunakan cara lain agar mendapatkan data dalam bentuk angka atau tipe data lainnya. Perhatikan kode program berikut!

```java
import java.io.*;

public class Buffered {
    public static void main(String[] args) {

        BufferedReader input = new BufferedReader(new InputStreamReader(System.in));

        try {
            System.out.print("Tahun lahir = ");
            int tahun = Integer.parseInt( input.readLine() );
            int umur = 2020 - tahun;

            System.out.println("Umur " + umur);
        } catch (IOException exception) {
            System.out.println("Error input!");
        }

    }
}
```

Perhatikan kode `Integer.parseInt()` pada kode program di atas! Method `parseInt()` adalah method untuk mengubah String menjadi int. Selain int, kita bisa gunakan method lainnya. Perhatikan tabel berikut!

| No   | Tipe data | Method                 |
| ---- | --------- | ---------------------- |
| 1    | int       | Integer.parseInt()     |
| 2    | double    | Double.parseDouble()   |
| 3    | boolean   | Boolean.parseBoolean() |

## Input File

Kita bisa mengambil input data dari file. Kode berikut adalah contoh program untuk mengakses data di dalam file.

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class InputFile {
    public static void main(String[] args) {

        try {
            Path file = Paths.get("src/data.txt");
            byte[] data = Files.readAllBytes(file);
            String isi = new String(data);
            System.out.println(isi);
        } catch (IOException exception) {
            System.out.println("File tidak ditemukan");
        }

    }
}
```

Jika kode program di atas dijalankan akan menghasilkan output seperti berikut.

```shell
Ini adalah data di dalam file data.txt
```

Output yang dihasilkan adalah data teks yang ada di dalam file yang diakses.

Tentunya kita harus memiliki sebuah file dengan nama `data.txt`. Jika tidakm maka program kita akan menghasilkan output yang berbeda, yaitu:

```shell
File tidak ditemukan
```

### Import 

Tidak lupa ketika kita menggunakan class untuk akses file dan lainnya untuk diimport ke dalam kode program yang kita buat. Setidaknya kita harus mengimpor beberapa class berikut.

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

....
```

Selanjutnya import tersebut dapat kita sederhanakan menjadi seperti berikut!

```java
import java.io.IOException;
import java.nio.*;
```

## Output File

Pada Java kita juga bisa menyimpan data ke dalam file. Fungsi ini berguna untuk menyimpan data-data penting yang akan digunakan kembali. Perhatikan kode program berikut ini!

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class OutputFile {
    public static void main(String[] args) {

        String isi = "Ini adalah data yang akan disimpan ke dalam file.";
        Path file = Paths.get("src/save.txt");

        try {
            Files.write(file, isi.getBytes());
        } catch (IOException exception) {
            System.out.println("Error saat menyimpan file.");
        }

    }
}

```

Jika kode program ini dijalankan, maka akan muncul sebuah file baru dengan nama `save.txt` pada folder `src`. Silahkan dicoba.

## Formating

Menampilkan teks ke layar juga merupakan teknik dasar dalam pemrograman Java. Biasanya kita menggunakan kode `System.out.println()` untuk menampilkan teks pada console. Selain kode tadi, kita bisa gunakan kode lain yang dapat diformat sesuai kebutuhan. Perhatikan kode program berikut ini!

```java
public class LearnFormating {
    public static void main(String[] args) {

        double pi = 22.0/7;
        System.out.printf("Pi = %f\n", pi);
        System.out.printf("Pi = %.2f\n", pi);

    }
}
```

Kode program tersebut jika dijalankan akan menghasilkan output sebagai berikut!

```shell
Pi = 3.142857
Pi = 3.14
```

Atau perhatikan juga kode program berikut!

```java
public class LearnFormating {
    public static void main(String[] args) {

        int harga = 16117250;
        System.out.println( harga );
        System.out.printf("%,d", harga);

    }
}
```

Kode program tadi akan menghasilkan output sebagai berikut.

```shell
16117250
16,117,250
```

Penggunaan kode `System.out.printf()` dapat menghasilkan format output yang lebih bagus. Pada contoh baris terakhir, data yang dioutputkan menggunakan thousand separator (tanda pisah ribuan, dalam bahasa Inggris).

Jika kita ingin menggunakan format dalam bahasa Indonesia, kita perlu menambahkan object Locale untuk bahasa Indonesia. Perhatikan kode program berikut!

```java
import java.util.Locale;

public class InScanner {
    public static void main(String[] args) {

        Locale bahasa = new Locale("id"); // Bahasa Indonesia

        int harga = 16117250;
        System.out.println( harga );
        System.out.printf("%,d \n", harga);
        System.out.printf(bahasa, "%,d \n", harga);

    }
}
```

