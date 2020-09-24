# Pemrograman Fundamental: File Handling

> Bla bla bla 

Menghandle file adalah hal yang harus ada dalam pemrograman Java. File-file yang ada dapat dibaca, diproses dan disimpan menjadi file-file baru akan membuat program semakin bermanfaat. 

Beberapa contoh sederhana program yang dapat memproses file adalah Notepad. Program tersebut dapat membaca file, mengubah dan menyimpan file hasil modifikasi ke dalam file baru.

Pada bab ini kita akan membahas tentang cara memeriksa file dan direktori, membaca file, menghapus, memindahkan serta meng-copy file dan direktori.

## Memeriksa file dan direktori

Sebelum melakukan proses pada sebuah file dan direktori, yang perlu kita pahami pertama kali adalah cara memeriksa file dan direktori. Memeriksa file dan direktori digunakan untuk memastikan keberadaan file atau direktori tersebut sebelum diproses. Selain itu, memeriksa file juga digunakan untuk memastikan apakah file tersebut bisa dibaca. Karena ada beberapa kondisi yang bisa menyebabkan file tidak dapat dibaca, diantaranya file rusak (corrupt) atau file yang sedang digunakan oleh program lain (used).

Perhatikan kode program berikut ini!

```java
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class CekFile {
    public static void main(String[] args) {

        Path file = Paths.get("src/hello.txt");

        if (!Files.exists(file)) {
            System.out.println("File tidak ditemukan.");
        } else if (!Files.isReadable(file)) {
            System.out.println("File tidak bisa dibaca.");
        } else {
            System.out.println("File siap diproses.");
        }

    }
}
```

Kode program di atas digunakan untuk memeriksa keberadaan file, selanjutnya memeriksa apakah file yang dimaksud bisa dibaca atau tidak. Kita bisa memanfaatkan teknik ini untuk mencegah kesalahan sebelum membaca file dan direktori.

Perhatikan variabel/object `file` pada kode program di atas. Variabel/object `file` tersebut merepresentasikan file atau folder di dalam komputer. Sedangkan method `Files.exists()` dan method `Files.isReadable()` adalah fungsi untuk mendapatkan status file tadi.

## Menghapus file dan direktori

Java dapat menghapus file, direktori dan link yang ada di komputer. Perhatikan kode program berikut!

```java
import java.io.IOException;
import java.nio.file.DirectoryNotEmptyException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class CekFile {
    public static void main(String[] args) {

        Path file = Paths.get("src/hello.txt");

        if (!Files.exists(file)) {
            System.out.println("File tidak ditemukan.");
        } else if (!Files.isReadable(file)) {
            System.out.println("File tidak bisa dibaca.");
        } else {
            System.out.println("File siap diproses.");

            // Menghapus file
            try {
                Files.delete(file);
            } catch (DirectoryNotEmptyException ex) {
                System.out.println("Direktori harus dikosongkan terlebih dahulu");
            } catch (IOException ex) {
                System.out.println("Tidak dapat menghapus file: " + file);
            }

        }
    }
}
```

Hati-hati dalam menghapus file menggunakan Java, karena dapat menyebabkan file terhapus dan tidak dapat dikembalikan. 

Java tidak dapat menghapus direktori yang berisi file, baik satu ataupun beberapa file. Sebaiknya direktori yang ingin dihapus harus dikosongkan dari file-file, setelah kosong baru direktori dapat dihapus.

Selain menggunakan method `Files.delete()` kita juga bisa menggunakan method `Files.deleteIfExists()` untuk menghapus file. 

```java
import java.io.IOException;
import java.nio.file.DirectoryNotEmptyException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class DelFile {
    public static void main(String[] args) {

        Path file = Paths.get("src/gofile");

        if (!Files.exists(file)) {
            System.out.println("File tidak ditemukan.");
        } else if (!Files.isReadable(file)) {
            System.out.println("File tidak bisa dibaca.");
        } else {
            System.out.println("File siap diproses.");

            // Menghapus file
            try {
                Files.deleteIfExists(file);
            } catch (DirectoryNotEmptyException ex) {
                System.out.println("Direktori harus dikosongkan terlebih dahulu");
            } catch (IOException ex) {
                System.out.println("Tidak dapat menghapus file: " + file);
            }
            
        }
    }
}
```

Perbedaan method `Files.delete()` dengan `Files.deleteIfExists()` adalah pada pemeriksaan filenya. Pada method `Files.delete()` tidak memeriksa keberadaan file, sehingga akan muncul exception jika file tidak ditemukan. 

## Meng-copy file dan direktori

Java dapat melakukan copy file atau direktori menggunakan method `Files.copy()`. Ketika Java melakukan copy direktori, maka Java hanya mengcopy direktori saja tanpa file yang ada di dalamnya. Perhatikan kode program berikut!

```java
import java.io.IOException;
import java.nio.file.DirectoryNotEmptyException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class CopyFile {
    public static void main(String[] args) {

        Path file = Paths.get("src/hello.txt");

        if (!Files.exists(file)) {
            System.out.println("File tidak ditemukan.");
        } else if (!Files.isReadable(file)) {
            System.out.println("File tidak bisa dibaca.");
        } else {
            System.out.println("File siap diproses.");

            // Copy file
            try {
                Path target = Paths.get("src/hello-new.txt");
                Files.copy(file, target);
            } catch (DirectoryNotEmptyException ex) {
                System.out.println("Direktori harus dikosongkan terlebih dahulu");
            } catch (IOException ex) {
                System.out.println("Tidak dapat menghapus file: " + file);
            }

        }
    }
}
```

Variabel/object `file` dan `target` adalah object dari class `Path`. Kita harus membuat kedua variabel/object ini untuk bisa melakukan copy pada Java. 

Pada saat melakukan copy file atau direktori, ada option tambahan yang bisa kita gunakan. Perhatikan contoh kode program berikut ini!

```java
import java.io.IOException;
import java.nio.file.*;

public class CekFile {
    public static void main(String[] args) {

        Path file = Paths.get("src/hello.txt");

        if (!Files.exists(file)) {
            System.out.println("File tidak ditemukan.");
        } else if (!Files.isReadable(file)) {
            System.out.println("File tidak bisa dibaca.");
        } else {
            System.out.println("File siap diproses.");

            // Copy file
            try {
                Path target = Paths.get("src/hello-new.txt");
                Files.copy(file, target, StandardCopyOption.REPLACE_EXISTING);
            } catch (DirectoryNotEmptyException ex) {
                System.out.println("Direktori harus dikosongkan terlebih dahulu");
            } catch (IOException ex) {
                System.out.println("Tidak dapat menghapus file: " + file);
            }

        }
    }
}
```

Pada method `Files.copy()` kita menambahkan `CopyOption` untuk pilihan tambahan. Kode program di atas menggunakan `StandardCopyOption.REPLACE_EXISTING` dengan tujuan me-replace (menimpa) file yang sudah ada. Berikut beberapa `CopyOption` yang bisa digunakan:

1. REPLACE_EXISTING, me-replace (menimpa) file yang sudah ada dengan file baru.
2. COPY_ATTRIBUTES, ikut meng-copy attribute file ke file baru.

## Memindahkan file dan direktori

Selain copy file, Java juga dapat move (memindahkan) file. Prosesnya sama persis dengan copy file. Perhatikan kode program berikut!

```java
import java.io.IOException;
import java.nio.file.*;

public class CekFile {
    public static void main(String[] args) {

        Path file = Paths.get("src/hello.txt");

        if (!Files.exists(file)) {
            System.out.println("File tidak ditemukan.");
        } else if (!Files.isReadable(file)) {
            System.out.println("File tidak bisa dibaca.");
        } else {
            System.out.println("File siap diproses.");

            // Copy file
            try {
                Path target = Paths.get("src/hello-new.txt");
                Files.move(file, target, StandardCopyOption.ATOMIC_MOVE);
            } catch (DirectoryNotEmptyException ex) {
                System.out.println("Direktori harus dikosongkan terlebih dahulu");
            } catch (IOException ex) {
                System.out.println("Tidak dapat menghapus file: " + file);
            }

        }
    }
}
```

Kita juga dapat menggunakan `CopyOption` yang sama dengan method `Files.copy()`. Tetapi ada option yang dapat digunakan khusus untuk method `Files.move()`, yaitu:

1. ATOMIC_MOVE, khusus untuk file system, atomic move memastikan semua akses ke file lama dipindahkan ke file baru.

## Menulis dan membaca file

Materi tentang menulis dan membaca file dijelaskan pada 