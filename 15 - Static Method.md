# Pemrograman Fundamental: Static Method

> Bla bla bla 



## Konsep dasar static method

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

## Parameter

## Tugas

