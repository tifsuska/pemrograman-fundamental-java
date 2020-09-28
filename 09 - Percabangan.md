# Pemrograman Fundamental: Percabangan

> Quote of the day

Programming itu isinya hanya percabangan dan perulangan. Jika diinputkan data A program akan berjalan dengan cara pertama, jika data B program akan berjalan dengan cara yang lain. Memahami percabangan dan perulangan adalah modal dasar membuat program.

## Konsep Dasar Percabangan

Setiap program berawal dari input data. Bentuk data bisa saja bermacam-macam. Data yang diinputkan akan diproses dan menghasilkan output. Perhatikan kembali gambar berikut!

![Input Proses Output](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/program.png)

Biasanya proses akan sangat bervariasi. Misalnya jika yang diinputkan adalah angka, maka proses yang digunakan adalah proses A. Sebaliknya jika yang diinputkan adalah String, maka proses yang digunakan adalah String.

Proses ini disebut dengan percabangan. Dengan demikian proses pada program akan jadi lebih dinamis.

Secara umum, percabangan terdiri dari 2 jenis, yaitu:

1. Percabangan dua, percabangan dua adalah yang paling dasar. Percabangan ini paling sering dan paling mudah digunakan. Biasanya menggunakan kondisi ya dan tidak, betul dan salah, dan sebagainya.
2. Percabangan lebih dari dua, dapat digunakan untuk kebutuhan khusus yang kurang tepat jika menggunakan percabangan dua. 

## Percabangan dalam bentuk flowchart

Dalam flowchart, percabangan dapat digambarkan seperti berikut.

![image-20200819211549539](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200819211549539.png)

Pada flowchart di atas terdapat percabangan yang ditentukan oleh sebuah kondisi. Apabila nilai yang diinputkan lebih besar sama dengan `55`, maka program akan menampilkan output `lulus`, tidak tidak maka ditampilkan output `gagal`.

Jika sudah memahami konsep percabangan dasar ini, maka kita akan mudah memanfaatkan percabangan untuk kasus-kasus pemrograman yang lebih kompleks.

Sebelum itu, kita perlu mengaplikasikan percabangan di dalam bahasa pemrograman Java, yaitu menggunakan if-else dan switch-case.

## Statement If else

Inilah statement yang bisa kita gunakan untuk membuat percabangan dua, perhatikan contoh kode program berikut ini!

```java
public class SimpleIf {
    public static void main(String[] args) {
        if (true) {
            System.out.println("Status: true");
        } else {
            System.out.println("Status: false");
        }
    }
}
```

Jika dijalankan, kode program di atas akan menghasilkan output berikut.

```shell
Status: true
```

Perhatikan kembali kode program di atas. Kita memiliki 2 baris kode `System.out.println()`, namun hanya 1 kode saja yang menghasilkan output. Hal ini wajar, karena kita menggunakan statement if-else. 

Statement if-else digunakan untuk percabangan. Artinya hanya akan menjalankan salah satu blok kode yang ada, blok if atau blok else.

![image-20200820085619282](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200820085619282.png)

Percabangan seperti ini dapat kita manfaatkan untuk banyak jenis program, dari yang sederhana sampai yang kompleks. 

Perhatikan kode program berikut ini!

```java
public class SimpleIf {
    public static void main(String[] args) {

        int nilai = 67;
        if (nilai > 55) {
            System.out.println("Anda lulus!");
        } else {
            System.out.println("Coba lagi!");
        }

    }
}
```

Kode program di atas jika dijalankan akan menghasilkan output seperti berikut!

```shell
Anda lulus!
```

Contoh program di atas dapat kita modifikasi menggunakan input Scanner agar program menjadi lebih bagus. Perhatikan kode program berikut!

```java
import java.util.Scanner;

public class SimpleIf {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Nilai: ");
        int nilai = input.nextInt();
        if (nilai > 55) {
            System.out.println("Anda lulus!");
        } else {
            System.out.println("Coba lagi!");
        }

    }
}
```

Sekarang program kita jadi lebih dinamis. Ketika program dijalankan, kita akan diminta untuk input `nilai` menggunakan `Scanner`. Jika kita inputkan angka 56 ke atas, maka akan keluar output `Anda lulus!`, sebaliknya akan keluar output `Coba lagi!`. Kedua output ini tidak akan pernah muncul bersamaan, karena berada pada blok if-else yang berbeda.

Di dalam blok if dan blok else kita dapat menulikan banyak kode program (statement). Semua jenis statement dapat dimasukkan ke dalam blok if dan blok else, termasuk control flow statement yang lainnya. Perhatikan kode program berikut!

```java
import java.util.Scanner;

public class SimpleIf {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Nilai: ");
        int nilai = input.nextInt();

        if (nilai > 55) {
            String output = "Anda lulus dengan nilai " + nilai;
            System.out.println( output );
        } else {
            String output = "Anda gagal! Silahkan coba lagi.";
            System.out.println( output );
        }

    }
}
```

Jika kita input nilai 86, maka kode program di atas akan menghasilkan output seperti berikut.

```shell
Nilai: 86
Anda lulus dengan nilai 86
```

## Statement If

Blok else sebenarnya tidak wajib. Kita bisa menggunakan blok else dan bisa juga tidak. Tentu disesuaikan dengan kebutuhan. Berikut adalah contoh program menggunakan statement if saja.

```java
import java.util.Scanner;

public class SimpleIf {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Nilai: ");
        int nilai = input.nextInt();

        if (nilai > 55) {
            String output = "Anda lulus dengan nilai " + nilai;
            System.out.println( output );
        }

        System.out.println( "Program Selesai" );

    }
}
```

Perbedaan dengan kode program if-else adalah hasil output pada setiap kondisi. Jika nilai yang diinputkan lebih besar dari 55, maka outputnya adalah

```shell
Nilai: 65
Anda lulus dengan nilai 65
Program Selesai
```

Tapi, jika nilai yang diinputkan kecil dari 55, maka hasilnya adalah

```shell
Nilai: 44
Program Selesai
```

Baris kode program `System.out.println( "Program Selesai" );` tetap muncul karena tidak berada di dalam blok if atau blok else. Inilah yang menyebabkan baris kode tersebut akan selalu dijalankan.

## Statement If else if

Statement if else if digunakan untuk melakukan percabangan lebih dari 2 cabang. Perhatikan kode program berikut!

```java
public class SimpleIf {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Nilai: ");
        int nilai = input.nextInt();

        if ( nilai > 75 ) {
            System.out.println("Sangat bagus!");
        } else if ( nilai > 55 ) {
            System.out.println("Bagus!");
        } else {
            System.out.println("Kurang!");
        }

    }
}
```

Dengan kode seperti di atas, maka program akan menghasilkan output yang lebih baik dari sebelumnya. Statement if else if sangat cocok diterapkan untuk kasus seperti ini.

Tapi, percabangan pada statement if else if sebenarnya penggunaan blok if di dalam blok if. Perhatikan ilustrasi berikut!

![image-20200820100524910](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200820100524910.png)

Pada kode program juga dapat kita modifikasi menjadi seperti berikut.

```java
import java.util.Scanner;

public class SimpleIf {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Nilai: ");
        int nilai = input.nextInt();

        if ( nilai > 75 ) {
            System.out.println("Sangat bagus!");
        } else {
            if ( nilai > 55 ) {
                System.out.println("Bagus!");
            } else {
                System.out.println("Kurang!");
            }
        }

    }
}
```

Hanya saja penulisan kode program seperti ini terlihat kurang optimal. Sehingga kita dapat memodifikasi kode program tersebut menjadi kode program sebelumnya.

## Latihan

Perhatikan kode program berikut! Lengkapi bagian kode yang ditandai sehingga program dapat berjalan dengan benar!

1. Kode program #1

   ```java
   import java.util.Scanner;
   
   public class BelajarIf {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.print("Input nilai (0-100) = ");
           int nilai = input.nextInt();
   
           if ( ............ ) {   //nilai 55 ke atas = lulus
               System.out.println("Selamat anda lulus!");
           } else {
               System.out.println("Anda gagal! Silahkan coba lagi!");
           }
   
       }
   }
   ```

   

2. Kode program #2

   ```java
   import java.util.Scanner;
   
   public class BelajarIf {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.print("Input angka = ");
           int angka = input.nextInt();
   
           if ( .............. ) { // habis dibagi 2 = genap
               System.out.println("Ini adalah angka genap!");
           } else {
               System.out.println("Ini adalah angka ganjil!");
           }
   
       }
   }
   ```

   

3. Kode program #3

   ```java
   import java.util.Scanner;
   
   public class BelajarIf {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.println("Aplikasi Hitung Berat Badan Ideal");
           System.out.println("=================================");
           System.out.println("Hai, silahkan isi data berikut!");
   
           System.out.print("Nama = ");
           String nama = input.nextLine();
   
           System.out.print("Tinggi badan (cm) = ");
           double tinggi = input.nextDouble();
   
           System.out.print("Berat badan (kg) = ");
           double berat = input.nextDouble();
   
           System.out.print("Tampilkan berat ideal seharusnya? (y/t) = ");
           String tampilkan = input.next();
   
           double ideal = tinggi - 100 - (tinggi - 100) / 10;
   
           if ( Math.abs( berat - ideal ) <= 1 ) {
               System.out.println("Berat badan anda sudah ideal!");
           } else if ( ................ ){  // jika lebih kecil dari ideal
               System.out.println("Anda terlalu kurus!");
           } else {
               System.out.println("Anda terlalu gemuk!");
           }
   
           if ( tampilkan.toLowerCase().equals("y") ) {
               System.out.println("Berat ideal anda = " + ideal);
           }
   
       }
   }
   ```

   

4. Kode program #4

   ```java
   import java.util.Scanner;
   
   public class BelajarIf {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.println("Aplikasi Login");
           System.out.println("==============");
           System.out.println("Selamat datang, silahkan login");
           System.out.println("terlebih dahulu!");
           System.out.println();
   
           System.out.print("Username: ");
           String username = input.nextLine();
   
           System.out.print("Password: ");
           String password = input.nextLine();
   
           if (username.equals("admin") && password.equals("1234")) {
               System.out.println("Hai Admin!");
           } else if ( .............. ) {  // usr = affan pwd = abcd
               System.out.println("Hai Affandes!");
           } else {
               System.out.println("Username atau password salah!");
           }
   
       }
   }
   ```

   

5. Kode program #5

   ```java
   import java.util.Scanner;
   
   public class BelajarIf {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.println("Aplikasi Saya");
           System.out.println("=============");
           System.out.println("Silahkan pilih:");
           System.out.println("1. Persegi panjang");
           System.out.println("2. Lingkaran");
           System.out.println("3. Keluar");
           System.out.println();
   
           System.out.print("Pilih [1-3] = ");
           int pilih = input.nextInt();
   
           if ( pilih == 1 ) {
               System.out.println("===============");
               System.out.println("Persegi Panjang");
               System.out.println("===============");
               System.out.println();
   
               System.out.print("Panjang = ");
               int panjang = input.nextInt();
               System.out.print("Lebar = ");
               int lebar = input.nextInt();
   
               System.out.println("Luas = " + (panjang *lebar));
           } else if ( ........... ) { // input pilihan ke 2
               System.out.println("===============");
               System.out.println("Lingkaran");
               System.out.println("===============");
               System.out.println();
   
               System.out.print("Jari-jari = ");
               int r = input.nextInt();
   
               System.out.println("Luas = " + (22 / 7 * r * r));
           }
   
           System.out.println("Terimakasih!");
       }
   }
   ```

   

## Switch case

Selain statement if-else, kita dapat gunakan statement switch-case untuk melakukan percabangan. Hanya saja, penggunaan statement switch-case tidak dapat diterapkan untuk semua kasus seperti pada statement if-else.

Perhatikan kode program berikut ini.

```java
public class SimpleSwitch {
    public static void main(String[] args) {
        int paket = 1;
        switch ( paket ) {
            case 1:
                System.out.println("Paket Regular");
                break;
            case 2:
                System.out.println("Paket Plus");
                break;
            case 3:
                System.out.println("Paket Premium");
                break;
            default:
                System.out.println("Tanpa Paket");
                break;
        }
    }
}
```

Dan kita pasti sudah bisa menebak output yang dihasilkan dari kode program di atas. Kode program tersebut juga dapat kita modifikasi menggunakan `Scanner`. Perhatikan kode program berikut!

```java
import java.util.Scanner;

public class SimpleSwitch {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Pilih paket (1-3) : ");
        int paket = input.nextInt();
        
        switch ( paket ) {
            case 1:
                System.out.println("Paket Regular");
                break;
            case 2:
                System.out.println("Paket Plus");
                break;
            case 3:
                System.out.println("Paket Premium");
                break;
            default:
                System.out.println("Tanpa Paket");
                break;
        }
    }
}
```

Dengan demikian kita bisa memasukkan data input paket sesuai dengan keinginan.

## Operator ternary

Operator ternary digunakan untuk mempersingkat statement if-else yang paling umum digunakan pada pemrograman. Perhatikan contoh program berikut ini!

```java
public class SimpleTernary {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Nilai : ");
        int nilai = input.nextInt();
        String hasil = "";

        if ( nilai >= 55 ) {
            hasil = "Lulus";
        } else {
            hasil = "Gagal";
        }

        System.out.println("Status: " + hasil);
    }
}
```

Kode program di atas terlihat banyak, dengan operator ternary dapat dipersingkat menjadi seperti berikut.

```java
public class SimpleSwitch {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.print("Nilai : ");
        int nilai = input.nextInt();
        String hasil = nilai >= 55 ? "Lulus" : "Gagal";

        System.out.println("Status: " + hasil);
    }
}
```

Jika memahami cara penggunaan operator ternary, maka banyak sekali kode program yang dapat dipersingkat untuk mendapatkan hasil yang sama.

## Nested block

Tantangan dalam membuat percabangan adalah ketika di dalam sebuah percabangan terdapat percabangan lainnya. Untuk itu kita perlu membahas bagaimana membuat percabangan bersarang (nested).

Perhatikan kode program berikut!

```java
public class SimpleNested {
    public static void main(String[] args) {

        int nilai = 77;

        if ( nilai > 55 ) {
            if ( nilai % 5 == 0 ) {
                System.out.println("Kelipatan 5 di atas 55");
            } else {
                System.out.println("Di atas 55");
            }
        } else {
            if ( nilai % 4 == 0 ) {
                System.out.println("Kelipatan 4 di bawah 55");
            } else {
                System.out.println("Di bawah 55");
            }
        }
        
    }
```

Pada kode program di atas, di dalam blok if dan blok else terdapat blok if-else baru. Masing-masing blok memiliki proses dan kalkulasi yang berbeda-beda.

## Latihan

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut dapat berjalan!

1. Kode program #1

   ```java
   import java.util.Scanner;
   
   public class BelajarBlok {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.println("Pilih jurusan:");
           System.out.println("1. Teknik Informatika");
           System.out.println("2. Sistem Informasi");
           System.out.print("Pilih [1-2] = ");
           int pilih = input.nextInt();
   
           switch (pilih) {
               case 1:
                   System.out.println("Selamat datang di Teknik Informatika.");
                   break;
               case 2:
                   System.out.println("Selamat datang di Sistem Informasi.");
                   break;
               default:
                   System.out.println("Jurusan ini tidak tersedia!");
           }
   
       }
   }
   ```

   

2. Kode program #2

   ```java
   import java.util.Scanner;
   
   public class BelajarBlok {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.print("Input angka = ");
           int angka = input.nextInt();
   
           String output = angka % 2 == 0 ? "genap" : "ganjil";
   
           System.out.printf("%d adalah %s", angka, output);
   
       }
   }
   ```

   

3. Kode program #3

   ```java
   import java.util.Scanner;
   
   public class BelajarBlok {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.println("Aplikasi Saya");
           System.out.println("=============");
           System.out.println("Silahkan pilih:");
           System.out.println("1. Persegi panjang");
           System.out.println("2. Lingkaran");
           System.out.println("3. Keluar");
           System.out.println();
   
           System.out.print("Pilih [1-3] = ");
           int pilih = input.nextInt();
   
           switch (pilih) {
               case 1:
                   System.out.println("===============");
                   System.out.println("Persegi Panjang");
                   System.out.println("===============");
                   System.out.println();
   
                   System.out.print("Panjang = ");
                   int panjang = input.nextInt();
                   System.out.print("Lebar = ");
                   int lebar = input.nextInt();
   
                   System.out.println("Luas = " + (panjang *lebar));
                   break;
               case 2:
                   System.out.println("===============");
                   System.out.println("Lingkaran");
                   System.out.println("===============");
                   System.out.println();
   
                   System.out.print("Jari-jari = ");
                   int r = input.nextInt();
   
                   System.out.println("Luas = " + (22 / 7 * r * r));
                   break;
           }
   
           System.out.println("Terimakasih!");
       }
   }
   ```

   

4. Kode program #4

   ```java
   import java.util.Scanner;
   
   public class BelajarIf {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.print("Input angka = ");
           int angka = input.nextInt();
   
           switch (angka) {
               case 1:
                   System.out.println("Step 1");
               case 2:
                   System.out.println("Step 2");
               case 3:
                   System.out.println("Step 3");
               case 4:
                   System.out.println("Step 4");
               case 5:
                   System.out.println("Step 5");
           }
       }
   }
   ```

   

5. Kode program #5

   ```java
   import java.util.Scanner;
   
   public class BelajarIf {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           System.out.print("Input angka = ");
           int angka = input.nextInt();
   
           switch (angka) {
               case 5:
                   System.out.println("Step 5");
               case 4:
                   System.out.println("Step 4");
               case 3:
                   System.out.println("Step 3");
               case 2:
                   System.out.println("Step 2");
               case 1:
                   System.out.println("Step 1");
           }
       }
   }
   ```

   

## Tugas

Buatlah resume tentang percabangan dengan menyertakan sumber-sumber lainnya sebagai bahan referensi tambahan/pelengkap!