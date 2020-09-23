# Programming Fundamentals: Exception

> Quote of the day

Jika program mengalami error, di Java kita sebut dengan istilah Exception. Mudahkan? Memahami Exception pada Java merupakan skill khas yang tidak banyak dimiliki oleh bahasa pemrograman lainnya. Tetapi, dengan menguasai skill ini, kita dapat membuat aplikasi yang lebih baik.

## Konsep dasar Exception

Exception biasanya muncul ketika ada kesalahan, atau proses yang mengakibatkan program berjalan tidak normal. Faktornya sangat banyak sekali. Perhatikan contoh program berikut ini!

```java
public class SimpelExc {
    public static void main(String[] args) {

        int nilai = 10;
        int hasil = nilai / (nilai-10);

        System.out.println(hasil);

    }
}

```

Jika kode program tersebut dijalankan, maka akan muncul exception seperti ini.

```shell
Exception in thread "main" java.lang.ArithmeticException: / by zero
	at exc.SimpelExc.main(SimpelExc.java:7)

Process finished with exit code 1
```

Dengan memahami cara kerja exception maka kita akan lebih mudah melakukan pencegahan apabila terjadi kesalahan. Inilah salah satu faktor yang membuat program kita lebih reliable.

## Try and catch

Semua exception dapat jika tidak dihandle akan mengakibatkan program kita berhenti (terminated). Tentunya hal ini akan mengurangi reliability dari program kita.

Salah satu cara untuk menghandle exception adalah dengan menggunakan statement try-catch. Perhatikan contoh program berikut!

```java
public class SimpelExc {
    public static void main(String[] args) {

        int nilai = 10;

        try {
            int hasil = nilai / (nilai-10);
            System.out.println(hasil);
        } catch (Exception exception) {
            System.out.println("Tidak boleh dibagi dengan 0");
        }

    }
}
```

Dengan menggunakan try-catch, maka program kita tidak akan berhenti tiba-tiba, tapi tetap berjalan dan menghasilkan output yang mudah dipahami.

```shell
Tidak boleh dibagi dengan 0

Process finished with exit code 0
```

Menggunakan try-catch akan membantu kita menghasilkan program yang lebih baik dan menghindari adanya error yang bisa memberhentikan program.

Kadang dalam kode program yang dibuat terdapat beberapa jenis exception, misalnya kode program berikut.

```java
import java.util.Scanner;

public class SimpelExc {
    public static void main(String[] args) {

        int[] data = {5, 2, 66, 32};
        Scanner input = new Scanner(System.in);
        System.out.print("Pilih angka [0-3] = ");
        int pilih = input.nextInt();
        System.out.print("Input pembagi = ");
        int bagi = input.nextInt();

        try {
            int hasil = data[pilih]/bagi;
            System.out.println("Hasil = " + hasil);
        } catch (ArithmeticException e) {
            System.out.println("Pembagi tidak boleh 0");
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Pilih angka 0 sampai 3 saja");
        }

    }
}
```

Apabila di dalam inputan kita pilih angka 5, maka outputnya akan menghasilkan pesan `Pilih angka 0 sampai 3 saja` sedangkan jika kita inputkan pembaginya adalah 0, maka outputnya adalah `Pembagi tidak boleh 0`. 

Dengan menggunakan catch lebih dari 1, kita bisa menghandle masing-masing jenis exception dengan tepat. 

## Finally

Biasanya block finally jarang sekali digunakan. Namun kita perlu mengetahui fungsi dari blok finally. Perhatikan kode program berikut!

```java
import java.util.Scanner;

public class SimpelExc {
    public static void main(String[] args) {

        int[] data = {5, 2, 66, 32};
        Scanner input = new Scanner(System.in);
        System.out.print("Pilih angka [0-3] = ");
        int pilih = input.nextInt();
        System.out.print("Input pembagi = ");
        int bagi = input.nextInt();

        try {
            int hasil = data[pilih]/bagi;
            System.out.println("Hasil = " + hasil);
        } catch (ArithmeticException e) {
            System.out.println("Pembagi tidak boleh 0");
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Pilih angka 0 sampai 3 saja");
        } finally {
            System.out.println("Proses selesai!");
        }

    }
}
```

Blok finally dijalankan setelah proses try-catch dijalankan. Baik terjadi exception maupun tidak. Karena fungsinya dapat digantikan dengan cara lain, makanya blok finally hampir jarang digunakan. Perhatikan kode program berikut ini!

```java
import java.util.Scanner;

public class SimpelExc {
    public static void main(String[] args) {

        int[] data = {5, 2, 66, 32};
        Scanner input = new Scanner(System.in);
        System.out.print("Pilih angka [0-3] = ");
        int pilih = input.nextInt();
        System.out.print("Input pembagi = ");
        int bagi = input.nextInt();

        try {
            int hasil = data[pilih]/bagi;
            System.out.println("Hasil = " + hasil);
        } catch (ArithmeticException e) {
            System.out.println("Pembagi tidak boleh 0");
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Pilih angka 0 sampai 3 saja");
        } 
        
        System.out.println("Proses selesai!");

    }
}
```

Kode program di atas juga menghasilkan output yang sama persis dengan kode sebelumnya. Sehingga ada atau tidak ada blok finally hasilnya akan sama.

## Tugas