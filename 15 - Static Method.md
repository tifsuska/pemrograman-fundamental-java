# Pemrograman Fundamental: Static Method

> Static method adalah langkah awal mempelajari Object Oriented Programming.



## Konsep dasar static method

Pada dasarnya, sebuah method (baik static maupun non-static) sama-sama memiliki tujuan yang sama. Yaitu memisahkan bagian proses menjadi sebuah proses yang dapat digunakan kembali.

Perhatikan kode program berikut!

```java
public class BelajarStaticMethod {
    public static void main(String[] args) {
        cetak();
    }
	// static method
    public static void cetak() {
        System.out.println("Salam programmer");
    }
}
```

Static method dengan nama `cetak()` pada kode program di atas adalah yang kita maksud. Static method berisi kode program juga, yang dapat dijalankan ketika dipanggil.

Ketika method tersebut dijalankan, maka kode program yang ada di dalam method akan dijalankan sampai selesai.

Uniknya, method tersebut dapat djalankan berkali-kali tanpa menulis ulang kode-kode program tersebut. Cukup dengan memanggil nama methodnya saja. Perhatikan kode program berikut!

```java
public class BelajarStaticMethod {
    public static void main(String[] args) {
        cetak();
        cetak();
        cetak();
    }

    public static void cetak() {
        System.out.println("Salam programmer");
    }
}
```



## Void dan Non-void

Static method ada 2 jenis, yaitu void dan non-void. Method void dapat langsung dijalankan dengan memanggil nama methodnya, sedangkan method non-void dapat menghasilkan data.

Perhatikan kode program berikut!

```java
public class BelajarStaticMethod {
    public static void main(String[] args) {
        
        // Jalankan static method void
        salam();
        
        // Jalankan static method non-void
        String teks = kalimat();
        System.out.println( teks );
        
    }
    
    // Static method void
    public static void salam() {
        System.out.println("Salam programmer!");
    }
    
    // Static method non-void
    public static String kalimat() {
        return "Apa kabar?";
    }
}
```

Dengan demikian, kita dapat memindahkan kode program yang terlalu panjang untuk disederhanakan menjadi sebuah method tersendiri.

Perhatikan kode program berikut!

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner scn = new Scanner(System.in);

        System.out.print("Panjang = ");
        double panjang = scn.nextDouble();

        System.out.print("Lebar = ");
        double lebar = scn.nextDouble();

        double luas = panjang * lebar;
        System.out.println("Luas = " + luas);
        
    }
}
```

Kode program di atas dapat kita sederhanakan menjadi kode program berikut ini.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        
        double panjang = inputPanjang();
        double lebar = inputLebar();
        double luas = panjang * lebar;
        cetakLuas(luas);

    }

    public static double inputPanjang() {
        Scanner scn = new Scanner(System.in);
        System.out.print("Panjang = ");
        return scn.nextDouble();
    }
    public static double inputLebar() {
        Scanner scn = new Scanner(System.in);
        System.out.print("Lebar = ");
        return scn.nextDouble();
    }
    public static void cetakLuas(double luas) {
        System.out.println("Luas = " + luas);
    }
}
```

Kok kodingnya jadi makin panjang?!

Tenang aja, masih ada cara lain yang lebih simple. Tapi setidaknya kita memahami dulu mengapa kita perlu method.

## Parameter

Di dalam static method kita bisa menggunakan parameter untuk memasukkan data-data yang diperlukan di dalam method. Perhatikan potongan kode berikut!

```java
public class Main {
    public static void main(String[] args) {
        
        // ...
        double luas = panjang * lebar;
        cetakLuas(luas);

    }
	
    // ...
    
    public static void cetakLuas(double l) {
        System.out.println("Luas = " + l);
    }
}
```

Variabel `luas` pada kode program di atas dapat digunakan oleh method `cetakLuas()` dengan cara menambahkan variabel tersebut ke dalam parameternya. Parameter yang digunakan di dalam method `cetakLuas()` dikenal sebagai parameter dengan nama `l`, bukan `luas`.

## Block, Variable Scope, Parameter dan Method

Ketika kita menggunakan method, kita harus ingat kembali materi tentang **block** sebelumnya. Setiap method memiliki block khusus. Hal ini akan membedakan variabel scope yang ada di dalamnya. 

Perhatikan kode program berikut!

```java
public class Main {
    public static void main(String[] args) {
        
        // ...
        double luas = panjang * lebar;
        cetakLuas(luas);

    }
	
    // ...
    
    public static void cetakLuas(double l) {
        System.out.println("Luas = " + l);
    }
}
```

Kode program di atas terdiri dari 2 static method, yaitu `main()` dan `cetakLuas()`. Setiap variabel yang di buat di dalam satu method, tidak dapat digunakan/dikenali pada method lainnya. Hal ini karena setiap method memiliki block yang berbeda-beda.

Pada kode program di atas, variabel `double luas` hanya dikenali di dalam method `main()`. Sedangkan variabel `double l` hanya dikenali di dalam method `cetakLuas()`, karena dideklarasikan di dalam parameter dari method `cetakLuas()`.

Dengan demikian, kita memiliki beberapa keuntungan dalam penulisan kode program, yaitu:

1. Tidak perlu khawatir menggunakan nama variabel yang sama dengan method lain.
2. Memisahkan kode program yang panjang menjadi bagian-bagian kode program yang lebih kecil.
3. Kode program dapat digunakan kembali secara independen.

Dengan begitu, kode program kita bisa lebih dinamis, cukup menulis kode program sekali saja, dapat dijalankan berulang-ulang.

Perhatikan kode program di atas, kita dapat menyederhanakan kode program tadi menjadi berikut.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        double panjang = input("Panjang = ");
        double lebar = input("Lebar = ");
        cetakLuas(panjang, lebar);

    }

    public static double input(String teks) {
        Scanner scn = new Scanner(System.in);
        System.out.print(teks);
        return scn.nextDouble();
    }
    public static void cetakLuas(double p, double l) {
        System.out.println("Luas = " + p*l);
    }
}

```



## Tugas

Buatlah sebuah resume tentang materi yang telah kita pelajari pada bab ini. Silahkan gunakan narasi masing-masing!