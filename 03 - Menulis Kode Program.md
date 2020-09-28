# Pemrograman Fundamental: Menulis Kode Program

> Menulis kode program adalah proses panjang untuk mewujudkan algoritma yang sudah kita buat supaya algoritma itu dapat berjalan dengan baik.

Jika kita ingin membangun sebuah rumah idaman, hal pertama yang kita lakukan adalah membuat sketsa atau gambar rumahnya. Setelah jadi, mulai kita hitung-hitung biaya yang mungkin dikeluarkan ketika membangun rumah tersebut. Setelah itu barulah rumah tadi dibangun. 

Proses ini sama persis ketika kita ingin membuat sebuah program, kita rancang algoritmanya, rancang tampilan aplikasinya. Setelah itu barulah kita tulis kode programnya (source code).

Maka, materi ini kita akan mulai menulis kode program dan menjalankan program tersebut. Supaya pembelajaran kita jadi lebih maksimal, sebaiknya kita sudah mempersiapkan kebutuhan yang harus ada sebelum melanjutkan ke pembahasan berikutnya.

Silakan lihat bagian persiapan belajar programming di bab [Pendahuluan](/pemrograman-fundamental-java-pendahuluan) untuk mengetahui persiapan apa saja yang harus kita siapkan. Kalo semua persiapan sudah dilakukan, saatnya kita mulai membuat program pertama.

## Program Salam

Ini adalah program pertama kita, silahkan jalankan program berikut!

```java
public class Salam {
    public static void main(String[] args) {
        System.out.println("Salam Programmer!");
    }
}
```

Jika kita belum tahu gimana cara menulis koding atau cara menjalankan kode program di atas, silakan pelajari salah satu materi berikut.

1. Materi [video Ngoding Java dari Nol](https://s.id/ngodingjava)
2. Artikel [Ngoding Java dari Nol](https://hynusantara.com/java-programming-dari-nol/)
3. Buku [Yuk Ngoding Java](https://s.id/ynjava)

Materi tentang ini sengaja kita pisahkan dari materi utama yang kita bahas. Karena materi tersebut sangat teknis sekali. Tinggal diikuti tahapannya, maka kita bisa membuat program dan menjalankan program di atas.

Pada materi ini kita bisa lebih fokus pada fundamental tentang konsep kerja sebuah program yang harus diketahui oleh programmer. 

## Bagaimana ouputnya?

Jika kita menjalankan program tadi dengan benar, maka hasilnya jadi seperti berikut.

```shell
Salam Programmer!
```

Ya, hanya muncul satu baris pesan `Salam Programmer!` pada layar komputer kita. Dengan begitu berarti kita sudah siap untuk memulai pemrograman Java dan mengikuti semua materi-materi pada artikel berikutnya.

## Kenali tentang PSVM

PSVM adalah singkatan dari **p**ublic **s**tatic **v**oid **m**ain. Yaitu blok yang digunakan untuk menjalankan kode program. Perhatikan kode program Salam tadi.

```java
public class Salam {
    public static void main(String[] args) {		// blok psvm
        System.out.println("Salam Programmer!");
    }												// tutup blok psvm
}
```

Nah, perhatikan blok psvm pada kode program di atas. Pada Java, blok psvm memang harus diketahui. Blok ini sangat penting karena inilah blok yang akan dijalankan oleh Java. Jika kita salah menuliskan blok psvm, bisa jadi program kita gak bisa jalan. Berikut bentuk dasar dari psvm.

```java
public static void main(String[] args) {
    ...
}
```

Blok psvm harus ditulis persis seperti itu, tidak perlu dimodifikasi. Setiap kali kita membuat kode program di Java, buat blok psvm ini pertama kali.

Semua kode program yang ada di dalam blok psvm ini akan dijalankan otomatis oleh Java. Jadi kalo di dalam blok ini tidak ditulis kode program, maka tidak akan ada yang bisa dijalankan.

Perhatikan kode program berikut.

```java
public class Mahasiswa {
    public static void main(String[] args) {		// blok psvm
        System.out.println("Salam Mahasiswa!");
    }												// tutup blok psvm
}
```

Pada kode program di atas, Java akan menjalankan kode program `System.out.println("Salam Mahasiswa!");` saja, karena hanya itu saja kode program yang ada di dalam blok psvm.

Walaupun kode program yang kita buat panjang, Java hanya melihat kode program yang ada di dalam blok psvm.

**Hanya saja**, blok psvm HARUS dibuat di dalam blok class. Dari contoh-contoh di atas, dapat kita lihat bahwa blok psvm dibuat di dalam blok **class Salam** dan blok **class Mahasiswa**.

```java
public class Salam {								// blok class Salam
    public static void main(String[] args) {		// blok psvm
        System.out.println("Salam Programmer!");
    }												// tutup blok psvm
}													// tutup blok class Salam
```

Nama class bisa apa saja, class Salam atau class Mahasiswa. PSVM dapat dibuat selagi dibuat di dalam blok class-nya. Tetapi jika dibuat di luar blok class maka program tidak akan berjalan. Ini adalah contoh kode program yang salah.

```java
public class Salam {								// blok class Salam
    
}													// tutup blok class Salam
public static void main(String[] args) {			// blok psvm
    System.out.println("Salam Programmer!");
}													// tutup blok psvm
```

Kode program tersebut tidak dapat dijalankan karena struktur psvm dibuat di luar class Salam. Hindari penulisan seperti tadi supaya tidak terjadi error.

Sampai pada tahapan ini kita sudah kenal tentang 5 baris kode program yang kita buat di awal. Memahami kode program tersebut memudahkan kita melanjutkan materi ke tahapan berikutnya.

## Apa yang terjadi saat program dijalankan?

Ketika kode program tadi dijalankan, komputer tidak langsung menjalankan kode program tersebut. Karena komputer sebenarnya tidak mengerti dengan kode program yang kita buat. 

Yang terjadi adalah kode program diubah menjadi bahasa mesin atau bahasa komputer. Setelah itu barulah dieksekusi oleh komputer.

![Bagaimana kode program berjalan](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/how-code-run.png)

Kalo kita sudah memahami bagaimana sebuah kode program bisa dieksekusi, kita akan paham bahwa apapun bahasa pemrogramannya, ketika akan dijalankan, kode program tersebut akan diterjemahkan dalam bentuk bahasa mesin dan dieksekusi/dijalankan dalam bentuk bahasa mesin.

Jika diperhatikan kode program Salam yang sudah kita buat tadi, kita mungkin saja heran mengapa ada kode program yang jumlah baris kodenya berjumlah 5 (lima) baris, ketika dijalankan kok hanya menghasilkan output `Salam Programmer!` saja?

Program sebenarnya hanya mengikut instruksi atau kode program yang dibuat. Pada contoh kita tadi, terdapat kode program `System.out.println('Salam Programmer!');` yang merupakan instruksi untuk menampilkan tulisan `Salam Programmer!` pada layar output. Karena instruksinya adalah menampilkan tulisan ke layar output, maka tulisan itulah yang muncul ketika program dijalankan.

Kalo pada program kita tidak terdapat instruksi untuk menampilkan tulisan ke layar output, maka tidak akan ada yang muncul di layar tersebut.

Perhatikan kode program berikut!

```java
public class Salam {
    public static void main(String[] args) {
        int nilai = 100 + 45;
    }
}
```

Maka sudah bisa dipastikan ketika program ini dijalankan, tidak akan ada output yang ditampilkan. Karena instruksi pada kode program tadi hanya menambahkan angka 100 dengan angka 45 menjadi 145. Walaupun angka tersebut sudah dijumlahkan, tetap saja tidak ada instruksi untuk menampilkan ke layar output. Jadi jangan heran kalo program ini dijalankan, tidak ada satupun angka 145 yang muncul di layar output.

## Bagaimana menulis program yang benar?

Menulis program harus mengikuti aturan-aturan sintaks yang berlaku. Beda bahasa pemrograman, beda pula aturan sintaksnya. Selain aturan sintaks, ada aturan lain yang harus kita ketahui untuk membuat kode program yang kita tulis menjadi lebih baik.

Untuk membuat kode program yang ditulis menjadi lebih baik, berikut beberapa hal yang perlu diketahui.

1. Case Sensitive
Sebagian besar bahasa pemrograman memiliki aturan case sensitive dalam penulisan nama. Artinya nama "pesan" akan dianggap berbeda dengan nama "Pesan" ataupun "PESAN". Dengan begitu penggunaan nama harus diperhatikan. Aturan ini disebut dengan case sensitive. Aturan case sensitive biasanya berlaku untuk nama variabel, nama fungsi dan nama class.
   
2. File
Setiap class pada Java ditulis ke dalam sebuah file dengan nama file sama persis dengan nama class-nya. Misalnya kita membuat class **Kotak**, maka class itu ditulis ke dalam file dengan nama **Kotak.java** dan disimpan di folder khusus.
   Aturan penulisan nama class adalah **menggabungkan** satu atau beberapa kata, dan diawal setiap kata menggunakan huruf kapital. Penulisan nama class dan nama file melarang penggunaan **spasi** pada nama.

   | Nama class yang disarankan | Nama class yang TIDAK disarankan    |
   | -------------------------- | ----------------------------------- |
   | Kotak                      | kotak atau KOTAK                    |
   | Files                      | FiLes                               |
   | BaseConnection             | baseconnection atau Base-Connection |
   | HtmlModel                  | HTMLModel                           |
   | StatusPeminjamanBuku       | status_peminjaman_buku              |
   
   Ketika sebuah class dibuat, pastikan class tersebut disimpan ke dalam file dengan nama yang sama persis dengan nama classnya. Perhatikan contoh berikut!

   | Nama class           | Nama file                 |
   | -------------------- | ------------------------- |
   | Kotak                | Kotak.java                |
   | Files                | Files.java                |
   | BaseConnection       | BaseConnection.java       |
   | HtmlModel            | HtmlModel.java            |
   | StatusPeminjamanBuku | StatusPeminjamanBuku.java |
   
3. Indentation
   Indentation digunakan untuk membedakan blok kode program agar mudah dibaca. Perhatikan kode program berikut ini!

   ```java
   public class Salam {
   public static void main(String[] args) {
   System.out.println("Salam Programmer!");
   }
   }
   ```

   Atau kode program berikut ini.

   ```java
   public class Salam {
   public static void main(String[] args) { System.out.println("Salam Programmer!");}
   }
   ```

   Penulisan kode program seperti di atas TIDAK DISARANKAN walaupun kode program tersebut tidak bermasalah ketika dijalankan. Hanya saja, kode program yang ditulis seharusnya memudahkan untuk dibaca dan dipahami oleh manusia. Mesin tidak pernah membaca kode program tersebut, tetapi programmer pasti akan membaca kode program tersebut.

## Gunakan komentar!

Kode program dibuat dengan benar dan teratur tujuannya adalah memudahkan dalam membaca dan memahami kode program tersebut. Kode program yang terlalu panjang atau terlalu banyak jumlah barisnya akan tetap mempersulit dalam memahami perintah yang dieksekusi. Dengan begitu kita dapat menggunakan komentar untuk memberikan dokumentasi dan catatan tentang kode program yang dimaksud.

Perhatikan contoh kode program berikut!

```java
/**
 * Gunakan komentar seperti ini untuk 
 * memberikan catatan yang cukup panjang
 */
package com.affandes.hynusa.c01;

public class Salam {
    public static void main(String[] args) {
        // Ini komentar pendek
        System.out.println("Salam Programmer!");
    }
}
```

Komentar sangat bermanfaat ketika kode program yang kita buat sudah cukup banyak. Kecil kemungkinan kita bisa mengingat semua kode program yang kita buat, ini membuat komentar menjadi sangat bermanfaat bagi kita untuk mengingat kode program tersebut. 

Perhatikan kode program berikut!

```java
public class BubbleSortBasic {
    public static void main(String[] args) {
        int[] data = {5,2,4,1,7,6,9,3,8};
        for (int i = 0; i < data.length; i++) {
            for (int j = 0; j < data.length-1; j++) {
                boolean isUrutanSesuai = data[j] < data[j+1];
                if (!isUrutanSesuai) {
                    int baru = data[j];
                    data[j] = data[j+1];
                    data[j+1] = baru;
                }
            }
        }
        for (int i = 0; i < data.length; i++) {
            System.out.println(data[i]);
        }
    }
}
```

Apa yang bisa kita pahami dari kode program di atas selain ini adalah proses BubbleSort? Gak ada, kita tidak mendapatkan informasi apa-apa selain nama class. Sedangkan kode-kode program yang ditulis harus dibaca lagi untuk mengetahui proses apa yang dilakukan oleh kode program tersebut.

Tapi, coba bandingkan dengan kode program yang memiliki komentar di bawah ini.

```java
/**
 * Ini adalah program untuk
 * menjalankan fungsi sorting
 * menggunakan algoritma
 * Bubble Sort
 *
 * Input: array int
 * Output: array int (sorted)
 *
 * contoh:
 * Input: {3,2,5,1}
 * Ouput: {1,2,3,5}
 */
public class BubbleSortBasic {
    public static void main(String[] args) {
        
        // Ini array input
        int[] data = {5,2,4,1,7,6,9,3,8};
        
        // Proses bubble sort
        for (int i = 0; i < data.length; i++) {
            for (int j = 0; j < data.length-1; j++) {
                boolean isUrutanSesuai = data[j] < data[j+1];
                if (!isUrutanSesuai) {
                    // swap data
                    int baru = data[j];
                    data[j] = data[j+1];
                    data[j+1] = baru;
                }
            }
        }
        
        // Tampilkan hasil array
        for (int i = 0; i < data.length; i++) {
            System.out.println(data[i]);
        }
        
    }
}
```

Penggunaan catatan dan informasi pada kode program di atas akan memudahkan kita memahami lebih cepat maksud dan tujuan kode program tersebut. Kita sebagai programmer akan terbantu mengetahui proses yang dilakukan oleh kode program tersebut tanpa harus membaca detail kode programmnya. Bagian mana yang merupakan data input, bagian mana yang merupakan proses menampilkan hasil sorting-nya.

### Cara membuat komentar

Banyak cara yang bisa digunakan untuk membuat komentar pada Java. Kita akan bahas satu persatu cara-caranya sebagai berikut.

1. Single line comment (komentar satu baris)
   Paling sering catatan yang dibuat adalah catatan singkat yang hanya satu baris. Java menggunakan karakter `//` (double slash) di awal komentar pada setiap baris. Lihat contoh berikut.
   
   ```java
   // ...
   // Komentar singkat
   int nilai = 10;
   double pi = 3.14;
   // ...
   ```
   Kita dapat membuat komentar di atas kode program yang akan kita komentari. Tidak ada batasan membuat komentar. Hanya saja komentar yang lebih dari satu baris harus menggunakan karakter `//` di awal setiap baris komentarnya. Lihat contoh berikut.
   ```java
   // ...
   // Deklarasi variabel
   // nilai dan pi
   int nilai;
   double pi = 3.14;
   // ...
   ```
   Cara di atas masih dimaklumi, namun tidak direkomendasikan. Karena kita masih bisa membuat komentar tersebut menjadi satu baris saja. Tapi, kalau memang kita ingin membuat komentar yang cukup panjang, ada baiknya kita gunakan multiline comment.
   Single line comment juga dapat digunakan di akhir sebuah baris kode program. Perhatikan contoh berikut.
   ```java
   // ...
   int nilai = 10; // nilai awal
   double pi = 3.14; // sebaiknya pake Math.PI
   // ...
   ```
   Membuat komentar di ujung setiap baris kode program dapat memudahkan kita membuat catatan rinci untuk satu baris tersebut. Sedangkan komentar di atas kode program bisa digunakan untuk catatan yang lebih umum. Perhatikan contoh komentar berikut ini.
      ```java
   // Program algoritma Bubble Sort
   public class BubbleSortBasic {
       public static void main(String[] args) {
           
           int[] data = {5,2,4,1,7,6,9,3,8}; // input array data int
           
           // Proses algoritma bubble sort (komentar lebih umum)
           for (int i = 0; i < data.length; i++) {
               for (int j = 0; j < data.length-1; j++) {
                   boolean isUrutanSesuai = data[j] < data[j+1];
                   if (!isUrutanSesuai) {
                       // swap data
                       int baru = data[j];
                       data[j] = data[j+1];
                       data[j+1] = baru;
                   }
               }
           }
           
           // Tampilkan hasil array (komentar lebih umum)
           for (int i = 0; i < data.length; i++) {
               System.out.println(data[i]); // print data indeks i
           }
       }
   }
      ```
   Semua dapat kita kasih komentar sesuai kebutuhan. Agar kode program yang kita buat dapat memudahkan kita mengingat kembali dan bahkan memahami kembali kode program tersebut.
   
2. Multiline comment (komentar banyak baris)
   Komentar dalam bentuk satu baris sangat praktis namun memiliki kekurangan. Perhatikan kode program berikut.
   ```java
   public class FiboSimple {
       public static void main(String[] args) {
           
           int x0 = 0; // Deklarasi x0
           int x1 = 1; // Deklarasi x1
           int n = 10; // Input n 
           
           // Pastikan n >= 0
           if (n >= 0) {
               System.out.println(x0); // Tulis 0
           }
           
           // Pastikan n >= 1
           if (n >= 1) {
               System.out.println(x1); // Tulis 1
           }
           
           // Untuk n >= 2, loop
           if (n >= 2) {
               // Loop 2 sampai n
               for (int i = 2; i < n; i++) {
                   // Hitung x1 + x0
                   int fn = x1 + x0;
                   System.out.println(fn);
                   x0 = x1; // Ubah x0
                   x1 = fn; // Ubah x1
               }
        	}
           
    	}
   }
   ```
   Penggunaan komentar di atas terasa sangat detail. Ini menyebabkan kita sebagai programmer justru semakin tidak terbantu. Penggunaan komentar yang terlalu banyak menunjukkan kode program tersebut perlu untuk dijelaskan dengan catatan yang lengkap.
   Multiline comment dapat digunakan untuk permasalahan tadi. Dengan membuat komentar yang lengkap, kita justru lebih terbantu dalam memahami kode program. Perhatikan kode program berikut.
   ```java
   public class FiboSimple {
       public static void main(String[] args) {

           // Deklarasi x0, x1 dan n
           int x0 = 0;
           int x1 = 1;
           int n = 10;
       
           /*
               * Jika n = 0 ==> x = 0
               * Jika n = 1 ==> x = 1
               * Jika n > 1 ==> x = x1 + x0
               */
           if (n >= 0) {
               System.out.println(x0); 
           }
           if (n >= 1) {
               System.out.println(x1); 
           }
           if (n >= 2) {
               for (int i = 2; i < n; i++) {
                   int fn = x1 + x0;
                   System.out.println(fn);
                   x0 = x1;
                   x1 = fn;
               }
           }
       
       }
   }
   ```
   Dengan menggunakan multiline comment kita bisa membuat catatan penjelasan yang lebih baik tentang kode program yang kita buat. Sehingga mengurangi jumlah komentar di dalam kode program. Karena terlalu banyak komentar dalam kode program juga akan mengganggu.

## Bagaimana jika terjadi error

Tidak ada kode program yang lepas dari error atau kesalahan. Terlebih lagi ketika dalam proses menulis kode program. Tapi, bukan berarti hal itu dibiarkan begitu saja. Mengetahui sumber error dan kesalahan dapat membantu kita memperbaiki kesalahan tersebut dengan cepat dan tepat. Perhatikan program berikut.

```java
public class Main {
    public static void main(String[] args) {
        int nilai = 10
        double pi = 3.14;
        System.out.println("Hasil = " + (nilai * pi));
    }
}
```

Kode program tersebut akan error kalo dijalankan. Berikut pesan errornya.

```shell
Main.java:3: error: ';' expected   
        int nilai = 10             
                      ^            
1 error                            
```

Ketika pesan error tampil, ada informasi yang bisa kita dapatkan untuk mencari tahu penyebab kesalahan yang muncul.

Pesan `Main.java:3` pada pesan error itu adalah sumber kesalahan yang menyebabkan pesan error muncul. Pesan tersebut artinya terjadi kesalahan pada file dengan nama `Main.java` pada kode program baris ke `3`. Sekarang kita lihat kode program sebelumnya.

```java
public class Main {	
    public static void main(String[] args) {
        int nilai = 10 									// baris ke 3
        double pi = 3.14;
        System.out.println("Hasil = " + (nilai * pi));
    }
}
```

Kesalahan yang terjadi pada baris ke `3` adalah `error: ';' expected` atau **tidak ada tanda ';' titik-koma** pada akhir baris kode program.

Mengetahui pesan error yang muncul merupakan skill dasar yang harus kita kuasai agar kita dapat lanjut belajar dengan mudah. Dengan demikian kita dapat dengan cepat dan tepat mengetahui kesalahan-kesalahan yang terjadi. 

## Latihan

Jawablah pertanyaan berikut sesuai dengan pemahaman masing-masing!

1. Apa itu source code?
2. Apa itu binary code?
3. Jelaskan proses yang terjadi ketika program dijalankan!
4. Jelaskan tentang psvm!
5. Apa saja panduan-panduan praktis menulis kode program yang benar?
6. Jelaskan jenis-jenis komentar pada Java!
7. Apa yang harus kita lakukan ketika terjadi error?

## Tugas

Carilah sebuah program sederhana dengan jumlah baris kurang dari 20 baris di internet. Kemudian ketik ulang kode programnya menggunakan aturan-aturan penulisan yang benar. Jangan lupa sertakan juga komentar yang diperlukan di dalam kode program tersebut!

