# Pemrograman Fundamental: Data, Variabel dan Tipe Data

> Setiap orang harus belajar pemrograman, karena pemrograman mengajarkan cara untuk berpikir. *Steve Jobs*

Data, variabel dan tipe data adalah awal permulaan membuat program. Materi dan pengetahuan tentang ketiga istilah ini bakal digunakan setiap kali kita membuat program. Tidak ada satupun program yang tidak memiliki konsep-konsep ini. Karena yang namanya program memang tentang mengelola data, variabel dan tipe data.

## Data dan variabel

Pada materi sebelumnya kita sudah praktik membuat program Salam, perhatikan kembali kode program berikut.

```java
public class Salam {
    public static void main(String[] args) {
        System.out.println("Salam Programmer!");
    }
}
```

Output `Salam Programmer!` adalah output yang dihasilkan oleh sebuah **teks atau String** yang ditulis pada kode program. Teks atau String `Salam Programmer!` ini disebut dengan **data**. Kebetulan datanya berupa teks, padahal data itu bukan hanya teks, bisa juga angka. 

### Data

Data yang kita buat pada kode program di atas dapat kita ubah sesuai dengan kebutuhan. Misalnya saya ingin mengubah data tersebut menjadi `Hai Programmer!`, maka kode program tadi akan berubah menjadi seperti berikut.

```java
public class Salam {
    public static void main(String[] args) {
        System.out.println("Hai Programmer!");
    }
}
```

Kita juga bisa membuat program kita menampilkan output 2 (dua) kali. Kode programmnya jadi berikut.

```java
public class Salam {
    public static void main(String[] args) {
        System.out.println("Hai Programmer!");
        System.out.println("Hai Programmer!");
    }
}
```

Jika kode program ini dijalankan, maka hasilnya outputnya jadi seperti ini.

```shell
Hai Programmer!
Hai Programmer!
```

Berikutnya kita akan membuat sebuah program yang menghasilkan output sebagai berikut.

```shell
Selamat datang.
Ini adalah program pertama saya.
Program ini saya beri nama MyApp.
```

Berikut adalah kode programnya.

```java
public class MyApp {
    public static void main(String[] args) {
        System.out.println("Selamat datang.");
        System.out.println("Ini adalah program pertama saya.");
        System.out.println("Program ini saya beri nama MyApp.");
    }
}
```

Simpel, kan? 

Selanjutnya kita bisa eksperimen dan eksplorasi menggunakan kombinasi kode program yang kita ketahui.

### Data teks vs data angka

Selain teks, data juga bisa dalam bentuk angka. Perhatikan kode berikut ini.

```java
public class DataAngka {
    public static void main(String[] args) {
        System.out.println(2020);
    }
}
```

Jika kode program tadi dijalankan, hasilnya jadi seperti berikut.

```shell
2020
```

Sebenarnya kode program di atas juga bisa kita buat jadi seperti ini.

```java
public class DataAngka {
    public static void main(String[] args) {
        System.out.println("2020");
    }
}
```

Dan jika dijalankan hasil outputnya akan sama dengan kode program sebelumnya. 

Dari dua kode program di atas, perbedaannya hanya pada tanda kutip ganda `"` saja. Angka `2020` yang tidak menggunakan tanda kutip ganda adalah **data angka**, sedangkan teks `"2020"` yang menggunakan tanda kutip ganda dalah **data teks**. 

Data angka dapat dilakukan operasi matematika, sedangkan data teks tidak dapat dilakukan operasi matematika.

Perhatikan contoh berikut ini.

```java
public class DataAngkaVsTeks {
    public static void main(String[] args) {
        System.out.println(20 + 30);		// outputnya 50
        System.out.println("20" + "30");	// outputnya 2030
    }
}
```

Kode program di atas akan menghasilkan output yang berbeda. Data angka `20 + 30` akan menghasilkan angka `50` karena menggunakan operasi penjumlahan angka. Sedangkan data teks `"20" + "30"` akan menghasilkan teks `2030` karena tidak dijumlahkan, hanya menggabungkan 2 teks menjadi satu.

Sehingga penggunaan angka dan teks harus disesuaikan dengan kebutuhan. Data angka bisa saja dijadikan teks, sedangkan data teks belum tentu bisa dijadikan data angka. Perhatikan contoh berikut.

```java
public class DataAngkaVsTeks {
    public static void main(String[] args) {
        System.out.println("Tahun " + 2020);	// outputnya Tahun 2020
        System.out.println(Tahun + "30");		// Error...
    }
}
```

Perhatikan juga kode program berikut ini.

```java
public class DataAngkaVsTeks {
    public static void main(String[] args) {
        System.out.println("Tahun " + 2020 + "Masehi"); 	// outputnya Tahun 2020
        System.out.println(12 + "kg");		// outputnya 12kg
        System.out.println("Rp" + 75000 + " rupiah");		// outputnya Rp75000 rupiah
    }
}
```

### Variabel

Simpelnya, variabel adalah tempat menyimpan data. Data yang disimpan akan dapat digunakan kembali berulang-ulang. Perhatikan contoh kode program berikut.

```java
public class Variabel {
    public static void main(String[] args) {
        String salam = "Salam Programmer!";
        System.out.println(salam);
        System.out.println(salam);
    }
}
```

Kita sudah punya sebuah variabel  `salam` pada kode program di atas. Variabel `salam` menyimpan data `"Salam Programmer!"` kemudian ditampilkan ke output. Proses ini menunjukkan tujuan mengapa variabel `salam` dibuat, yaitu dapat digunakan kembali berulang-ulang tanpa harus menuliskan datanya berulang-ulang. Perhatikan hasil outputnya.

```shell
Salam Programmer!
Salam Programmer!
```

Variabel ini akan semakin bermanfaat ketika data yang disimpan cukup banyak, misalnya seperti kode program berikut.

```java
public class Variabel {
    public static void main(String[] args) {
        String salam = "Selamat datang di aplikasi pertama saya, MyApp.";
        System.out.println(salam);
        System.out.println(salam);
    }
}
```

Ketika sebuah variabel dibuat dengan nama `salam` atau apapun namanya, kita bisa gunakan nama tersebut untuk mendapatkan data yang disimpan oleh variabel tersebut. Pada contoh di atas kita menggunakan nama `salam` di dalam kode `System.out.println(salam);`. 

Perlu diingat bahwa penggunaan nama `salam` sebagai variabel tidak menggunakan tanda kutip ganda. Karena penggunaan tanda kutip ganda hanya untuk data teks saja, bukan nama variabel.

Apa jadinya jika kita menggunakan tanda kutip ganda pada nama variabel? Perhatikan contoh berikut.

```java
public class Variabel {
    public static void main(String[] args) {
        String salam = "Salam Programmer!";
        System.out.println("salam");
        System.out.println("salam");
    }
}
```

Kode program di atas akan menghasilkan output seperti berikut.

```shell
salam
salam
```

Untuk itu penggunaan tanda kutip ganda sangat perlu diperhatikan. Jangan sampai kita bingung dengan konsep seperti tadi. Karena akan berakibat fatal jika jita salah menggunakannya.

### Memberi nama pada variabel

Setiap variabel harus memiliki nama (identifier) yang unik, agar dapat dikenali oleh program dengan jelas. Berikut beberapa hal yang perlu diketahui tentang penamaan pada variabel, yaitu:

1. Bersifat case-sensitive, 
2. Terdiri dari alfanumerik dan beberapa simbol
3. Tidak menggunakan spasi, titik dan koma
4. Tidak diawali dengan angka

Adapun saran dan rekomendasi dalam membuat nama variabel adalah

1. Singkat, nama variabel harus singkat agar kode program terlihat bagus.
2. Bermakna, nama variabel sebaiknya mewakili isi datanya. Menggunakan nama variabel `x` untuk menyimpan data nama mahasiswa akan mempersulit mengingat nama variabelnya. 
3. Camel case, misalnya `nama` atau `namaMahasiswa` atau `namaMahasiswaBaru` merupakan penulisan nama dengan camel case.

### Latihan memahami data

Sebelum kita melanjutkan ke materi berikutnya, silahkan kerjakan latihan berikut untuk memudahkan kita mengingat konsep-konsep yang kita sampaikan sebelumnya.

Perhatikan kode program berikut! Tanpa menjalankan kode program di bawah ini, tebaklah output yang dihasilkan oleh kode program tersebut. Kemudian cocokkan dengan hasil output setelah kode program dijalankan.

1. Kode program #1

   ```java
   public class Latihan01 {
       public static void main(String[] args) {
           System.out.println("Selamat datang.");
           System.out.println("Di MyApp versi 1.0");
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class Latihan02 {
       public static void main(String[] args) {
           System.out.print("Selamat datang.");
           System.out.print("Di MyApp versi 1.0");
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class Latihan03 {
       public static void main(String[] args) {
           System.out.println("Selamat datang." + "Di MyApp versi 1.0");
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class Latihan04 {
       public static void main(String[] args) {
           System.out.println("Selamat datang.\n" + "Di MyApp versi 1.0");
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class Latihan05 {
       public static void main(String[] args) {
           System.out.print("Selamat datang.\n" + "Di MyApp versi 1.0");
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class Latihan06 {
       public static void main(String[] args) {
           System.out.println("Selamat datang.\n" + "Di MyApp versi 1.0");
           System.out.println("Dibuat oleh Affandes");
       }
   }
   ```

   

7. Kode program #7

   ```java
   public class Latihan07 {
       public static void main(String[] args) {
           System.out.print("Selamat datang.\n" + "Di MyApp versi 1.0");
           System.out.print("Dibuat oleh Affandes");
       }
   }
   ```

   

8. Kode program #8

   ```java
   public class Latihan08 {
       public static void main(String[] args) {
           System.out.print("Dibuat oleh Affandes");
           System.out.print("Selamat datang.\n" + "Di MyApp versi 1.0");
       }
   }
   ```

   

9. Kode program #9

   ```java
   public class Latihan09 {
       public static void main(String[] args) {
           System.out.print("Dibuat oleh Affandes");
           System.out.print("Selamat datang.\n" + "Di MyApp versi 1.0");
       }
   }
   ```

   

10. Kode program #10

    ```java
    public class Latihan09 {
        public static void main(String[] args) {
            System.out.print("Dibuat oleh Affandes");
            
            
            
            System.out.print("Selamat datang.\n" + "Di MyApp versi 1.0");
        }
    }
    ```


### Latihan memahami data teks dan data angka

Latihan kali ini membantu kita untuk memahami konsep perbedaan antara data teks dan data angka. 

Perhatikan kode program berikut ini. Tanpa menjalankan kode program terlebih dahulu, tuliskan output yang dihasilkan, kemudian bandingkan dengan hasil output sebenarnya.

1. Kode program #1

   ```java
   public class Latihan01 {
       public static void main(String[] args) {
           System.out.println("Jumlah 5 + 6 = " + 5 + 6);
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class Latihan02 {
       public static void main(String[] args) {
           System.out.println("Jumlah 5 + 6 = " + (5 + 6));
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class Latihan03 {
       public static void main(String[] args) {
           System.out.println("Jumlah 5 - 6 = " + (5 - 6));
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class Latihan04 {
       public static void main(String[] args) {
           System.out.println("Jumlah 5 - 6 = " + 5 - 6);
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class Latihan05 {
       public static void main(String[] args) {
           System.out.println("Hasil 5 x 6 = " + 5 * 6);
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class Latihan06 {
       public static void main(String[] args) {
           System.out.println("Hasil 5 / 6 = " + 5 / 6);
       }
   }
   ```

   

7. Kode program #7

   ```java
   public class Latihan07 {
       public static void main(String[] args) {
               System.out.println(2 + 3 + " = lima");
       }
   }
   ```

   

8. Kode program #8

   ```java
   public class Latihan08 {
       public static void main(String[] args) {
           System.out.println("Nama \t: " + "Budi");
           System.out.println("Nilai \t: " + (77+82+69)/3);
       }
   }
   ```

   

9. Kode program #9

   ```java
   public class Latihan09 {
       public static void main(String[] args) {
           System.out.println(2 + 3 + " = " + "2" + "3");
       }
   }
   ```

   

10. Kode program #10

    ```java
    public class Latihan10 {
        public static void main(String[] args) {
            System.out.println(2 + 3 + " = " + ("2" + "3"));
        }
    }
    ```

    

### Latihan memahami variabel

Latihan ini membantu kita mengingat konsep dan memahami materi tentang variabel pada Java. 

Perhatikan kode program berikut ini. Tanpa menjalankan kode program tersebut terlebih dahulu, tuliskan output yang akan ditampilkan. Kemudian bandingkan dengan output yang sebenarnya.

1. Kode program #1

   ```java
   public class Latihan01 {
       public static void main(String[] args) {
           String nama = "Budi";
           System.out.println( nama );
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class Latihan02 {
       public static void main(String[] args) {
           String nama = "Budi";
           System.out.println( "Hai" + " " + nama );
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class Latihan03 {
       public static void main(String[] args) {
           String sapa = "Hai";
           String nama = "Budi";
           System.out.println( sapa + " " + nama );
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class Latihan04 {
       public static void main(String[] args) {
           String nama = "Budi";
           System.out.println("Hai " + nama );
           System.out.println("Selamat datang di MyApp.");
           System.out.println("========================");
           System.out.println("Terimakasih " + nama + " sudah membeli aplikasi ini.");
           System.out.println("Support: support@myapp.co.id");
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class Latihan05 {
       public static void main(String[] args) {
           String nama = "Budi";
           String teks = "Hai " + nama;
           System.out.println( teks );
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class Latihan06 {
       public static void main(String[] args) {
           
           String nama = "Budi";
           String teks01 = "Hai " + nama;
           String teks02 = "Selamat datang di MyApp.";
           String teks03 = "========================";
           String teks04 = "Terimakasih " + nama + " sudah membeli aplikasi ini.";
           String teks05 = "Support: support@myapp.co.id";
           
           System.out.println( teks01 );
           System.out.println( teks02 );
           System.out.println( teks03 );
           System.out.println( teks04 );
           System.out.println( teks05 );
       }
   }
   ```

   

7. Kode program #7

   ```java
   public class Latihan07 {
       public static void main(String[] args) {
           
           String nama = "Budi";
           String teks01 = "Hai " + nama + "\n";
           String teks02 = "Selamat datang di MyApp.\n";
           String teks03 = "========================\n";
           String teks04 = "Terimakasih " + nama + " sudah membeli aplikasi ini.\n";
           String teks05 = "Support: support@myapp.co.id";
           
           System.out.println( teks01 + teks02 + teks03 + teks04 + teks05 );
       }
   }
   ```

   

8. Kode porgram #8

   ```java
   public class Latihan08 {
       public static void main(String[] args) {
           
           String nama = "Budi";
           String teks01 = "Hai " + nama;
           String teks02 = "Selamat datang di MyApp.";
           String teks03 = "========================";
           String teks04 = "Terimakasih " + nama + " sudah membeli aplikasi ini.";
           String teks05 = "Support: support@myapp.co.id";
           
           System.out.println( 
               teks01 + "\n" + teks02 + "\n" + 
               teks03 + "\n" + teks04 + "\n" + teks05 );
       }
   }
   ```

   

9. Kode program #9

   ```java
   public class Latihan09 {
       public static void main(String[] args) {
           String nama = "Budi";
           String nilai = "87";
           String bonus = "5";
           System.out.println( "Nama : " + nama );
           System.out.println( "Nilai : " + nilai );
           System.out.println( "Total : " + nilai + bonus );
       }
   }
   ```

   

10. Kode program #10

    ```java
    public class Latihan10 {
        public static void main(String[] args) {
            String nama = "Asep";
            String nama = "Budi";
            System.out.println( "Hai" + " " + nama );
        }
    }
    ```

    

### Deklarasi dan inisialisasi variabel

Perlu bagi kita untuk mengetahui tentang deklarasi dan inisialisasi yang dilakukan oleh variabel. Apapun jenis variabelnya pasti akan berurusan dengan deklarasi atau inisialisasi. Kedua proses ini cukup mudah dipahami, tapi kita akan temukan error atau kesalahan jika kita salah melakukan kedua proses ini.

Perhatikan kode program berikut ini.

```java
public class DeklarasiInisialisasi {
    public static void main(String[] args) {
        
        // Deklarasi
        String label;
        
        // Inisialisasi
        String nama = "Budi";
        String teks01 = "Hai " + nama;
        String teks02 = "Apa kabar?";
		
        // Output
        System.out.println(teks01 + ". " + teks02);
    }
}
```

Pada kode program di atas kita melakukan proses inisialisasi variabel `nama`, variabel `teks01` dan variabel `teks02`. Masing-masing memiliki data yang disimpan. Sedangkan pada variabel `label` kita melakukan proses deklarasi.

Untuk memudahkan kita memahami deklarasi dan inisialisasi, perhatikan potongan kode program berikut!

![Deklarasi dan Inisialisasi](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200711083712350.png)

Bagian deklarasi pada kode program tersebut adalah `String label`, sedangkan bagian inisialisasi adalah `String nama = "Budi"` (tanpa tanda titik-koma, ya). 

Pada saat deklarasi, kita menentukan nama dan tipe data sebuah variabel, sedangkan pada saat inisialisasi, kita melakukan deklarasi sekaligus menyimpan data awal pada variabel yang dideklarasikan.

Variabel yang sudah dideklarasikan tidak dapat dideklarasi ulang, ataupun diinisialisasi ulang. Begitu juga sebaliknya, variabel yang sudah diinisialisasi tidak dapat dideklarasi ulang ataupun diinisialisasi ulang.

Perhatikan kode program berikut.

```java
public class DeklarasiInisialisasi {
    public static void main(String[] args) {
        
        // Deklarasi 
        String nama;
        String teks01;
        String teks02;
        
        // Inisialisasi 
        String nama = "Budi";			// Error
        String teks01 = "Hai " + nama;	// Error
        String teks02 = "Apa kabar?";	// Error
        
		// Output
        System.out.println(teks01 + ". " + teks02);
    }
}
```

Variabel `nama` tidak dapat diinisialisasi ulang, karena pada baris sebelumnya variabel `nama` sudah dideklarasikan. Sehingga kode program di atas akan menghasilkan error ketika dijalankan.

### Assignment

Selain deklarasi dan inisialisasi, ada istilah lain yaitu assignment (saya sulit mencari padanan katanya di dalam bahasa Indonesia). Supaya mudah memahami, perhatikan kode program berikut ini.

```java
public class InitAssign {
    public static void main(String[] args) {
        
        // Deklarasi
        String label;
        
        // Inisialisasi
        String nama = "Budi";
        
        // Assignment
        label = "Mahasiswa";
        
        // Assignment
        nama = "Candra";
        
    }
}
```

Assignment mudahnya adalah menyimpan data ke dalam variabel yang sudah dideklarasi atau diinisialisasi. Apabila terdapat data di dalam variabel tersebut sebelumnya, maka data sebelumnya akan ditimpa dan terhapus, digantikan oleh data yang baru.

Proses aasignment hanya dapat dilakukan pada variabel yang sudah dideklarasikan atau sudah diinisialisasikan sebelumnya. Perhatikan kode program berikut ini.

```java
public class InitAssign {
    public static void main(String[] args) {
        
        // Assignment
        nama = "Budi";		// Error
        
        // Deklarasi
        String nama;
        
    }
}
```

Kode program di atas tidak akan bisa dijalankan karena ada error saat menggunakan assignment sebelum deklarasi. Deklarasi variabel `nama` harus dilakukan terlebih dahulu sebelum assignment variabel `nama`. Jika tidak, maka error sudah pasti muncul. Perhatikan lagi kode berikut.

```java
public class DeklarasiInisialisasi {
    public static void main(String[] args) {
        
        String nama;
        String teks01;
        
        nama = "Budi";
        
        String teks02;
        
        teks01 = "Hai " + nama;
        teks02 = "Apa kabar?";
        
		// Output
        System.out.println(teks01 + ". " + teks02);
    }
}
```

Kode program di atas akan berjalan dengan baik, tanpa ada error. Ini karena semua proses assignment masing-masing variabel dilakukan setelah proses deklarasi variabel tersebut. Perhatikan variabel `nama` di atas. Deklarasi variabel `nama` sudah dilakukan terlebih dahulu pada baris awal, sedangkan assignment-nya dilakukan beberapa baris setelahnya.

Jika kita coba menjalankan kode program berikut, maka tidak akan bisa berjalan. Karena kode program berikut memiliki error.

```java
public class InitAssign {
    public static void main(String[] args) {
        
        // Deklarasi
        String nama;
        
        // output nama
        System.out.println( nama ); // Error
        
        // Assignment
        nama = "Budi";
        
    }
}
```

Error muncul karena variabel `nama` belum memiliki data apapun atau belum diinisialisasi. Sehingga variabel `nama` tidak dapat di-output-kan. Supaya variabel `nama` dapat digunakan setelah deklarasi, lakukan assignment terhadap variabel `nama`, contohnya seperti kode berikut.

```java
public class InitAssign {
    public static void main(String[] args) {
        
        // Deklarasi
        String nama;
        
        // Assignment
        nama = "Budi";
        
        // output nama
        System.out.println( nama ); // Outputnya "Budi"
        
        // Assignment
        nama = "Candra";
        
    }
}
```

Dengan demikian, variabel `nama` telah menyimpan data `"Budi"` dan dapat digunakan untuk output atau proses lainnya.

Lain halnya jika kode program berikut kita jalankan.

```java
public class InitAssign {
    public static void main(String[] args) {
        
        // Inisialisasi
        String nama = "Budi";
        
        // output nama
        System.out.println( nama ); // output "Budi"
        
        // Assignment
        nama = "Andi";
        
    }
}
```

Kode program di atas berjalan dengan baik dan menghasilkan output `Budi`. Variabel `nama` akhirnya memiliki data `"Budi"` setelah dilakukan proses inisialisasi. 

Terakhir, ketika kode program kita ubah menjadi berikut.

```java
public class InitAssign {
    public static void main(String[] args) {
        
        // Inisialisasi
        String nama = "Budi";
        
        // Assignment
        nama = "Andi";
        
        // output nama
        System.out.println( nama ); // output "Andi"
        
        // Assignment
        nama = "Candra";
        
    }
}
```

Maka output yang dihasilkan adalah `Andi`. Variabel `nama` menyimpan data `"Andi"` dan menghapus data `"Budi"` setelah melakukan proses assignment pada variabel `nama`. Proses assignment ini dapat dilakukan berkali-kali sesuai kebutuhan. Setiap kali proses assignment dilakukan, maka variabel akan menghapus data sebelumnya.

### Latihan memahami deklarasi, inisialisasi dan assignment

Perhatikan kode program berikut ini. Identifikasi kesalahan dalam penggunaan deklarasi, inisialisasi ataupun assignment pada kode program berikut. Kemudian lakukan perbaikan untuk mendapatkan kode program yang seharusnya benar.

1. Kode program #1

   ```java
   public class Latihan01 {
       public static void main(String[] args) {
           
           String nama;
           string = "Andi";
           
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class Latihan02 {
       public static void main(String[] args) {
           
           String nama = "Budi";
           string = "Andi";
           
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class Latihan03 {
       public static void main(String[] args) {
           
           string = "Andi";
           String string;
           
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class Latihan04 {
       public static void main(String[] args) {
           
           String nama, nim;
           nim = "1234";
           nama = "Andi";
           
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class Latihan05 {
       public static void main(String[] args) {
           
           String nama = "Andi", nim = "1234";
           nama = "Budi";
           nim = "4321";
           
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class Latihan06 {
       public static void main(String[] args) {
           
           String nama = "Andi"; String nim = "1234";
           nama = "Budi";
           nim = "4321";
           
       }
   }
   ```

   

7. Kode program #7

   ```java
   public class Latihan07 {
       public static void main(String[] args) {
           
           String nama1 = "Andi"; nim1 = "1234";
           String nama2 = nama1; nim2 = nim1;
           
           System.out.println(nama1);
           System.out.println(nama2);
           
       }
   }
   ```

   

8. Kode program #8

   ```java
   public class Latihan08 {
       public static void main(String[] args) {
           
           String nama1 = "Andi"; nim1 = "1234";
           String nama2 = nama1; nim2 = nim1;
           
           System.out.println(nama1);
           System.out.println(nama2);
           
       }
   }
   ```

   

## Tipe data

Pada saat deklarasi atau inisialisasi, kita menentukan tipe data apa yang digunakan pada variabel yang dideklarasi. Perhatikan ilustrasi berikut.

![Data, Variabel dan Tipe Data](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/data-var-tipe.png)

Gambar tersebut adalah inisialisasi sebuah variabel dengan tipe data String. Tipe data String adalah tipe data khusus untuk menyimpan data teks. Makanya variabel `nama` yang kita buat menyimpan sebuah teks yaitu `"Budi"`. 

Variabel dengan tipe data String **tidak bisa** menyimpan data angka, misalnya contoh kode program berikut.

```java
public class TipeData {
    public static void main(String[] args) {
        
        // Error, String tidak dapat menyimpan angka
        String nilai = 10;
        
		// Output
        System.out.println( nilai );
    }
}
```

Kode program tersebut akan error, karena tidak bisa menyimpan data angka di dalam variabel bertipe data String. Data angka harus disimpan ke variabel bertipe data angka, misalnya int. Perhatikan kode program berikut.

```java
public class TipeData {
    public static void main(String[] args) {
        
        // Inisialisasi variabel bertipe data int
        int nilai = 10;
        
		// Output
        System.out.println( nilai );
    }
}
```

Di dalam pemrograman Java, terdapat beberapa tipe data yang dapat digunakan dalam pemrograman. Berikut adalah kategori dari tipe data di Java:

1. Tipe data primitif
Tipe data primitif di Java adalah tipe data yang memang sudah built-in (bawaan) dan merupakan tipe data dasar di Java. Tipe data primitif terbagi menjadi beberapa bagian. Secara rinci dapat di perhatikan ilustrasi berikut.
   
![Tipe Data Primitif](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/tipe-data-primitif.png)
   
Tipe data primitif yang dapat digunakan pada Java berjumlah 8 tipe data (simbol kotak abu-abu). Kita dapat menggunakan tipe data tersebut sesuai kebutuhan. Perhatikan kode program berikut.
   
```java
   public class TipeData {
       public static void main(String[] args) {
           
           byte myByte = 2;
           short myShort = 500;
           int myInt = 20000;
           long myLong = 5000000;
           
           float myFloat = 4.25f;
           double myDouble = 3.14;
           
           char myChar = 'A';
           boolean myBoolean = false;
           
       }
   }
   ```
   
Kode program di atas adalah contoh penggunaan tipe data primitif pada saat inisialisasi variabel. Setiap kali membuat sebuah variabel, pastikan kita menentukan tipe datanya terlebih dahulu. Ketika tipe data sudah ditentukan, maka kita tidak dapat melakukan perubahan tipe data ataupun perubahan nama variabel.
   
```java
   public class TipeData {
       public static void main(String[] args) {
           
           int nilai = 78;
           
           long nilai = 88; // Error
           
       }
   }
   ```
   
Kode program di atas akan error karena variabel nilai tidak dapat diinisialisasi ulang menjadi tipe data yang berbeda.
   
2. Tipe data non-primitif
Sedangkan tipe data non-primitif merupakan class yang digunakan sebagai tipe data. Kita dapat membuat tipe data sendiri menggunakan class. Salah satu contoh tipe data non-primitif adalah String. 

## Tipe data String

Sebenarnya kita sudah familiar dengan tipe data String, karena kita sudah sering menggunakan tipe data String pada kode program kita sebelumnya. Sekarang waktunya kita memahami tentang tipe data String. Perhatikan kode program berikut.

```java
public class TipeDataString {
    public static void main(String[] args) {
        
        // Inisialisasi variabel dengan tipe data String
        String nama = "Budi";
        
		// Output
        System.out.println( nama );
    }
}
```

Kode program di atas contoh mendeklarasikan sebuah variabel dengan tipe data String. Variabel tersebut kita beri nama `nama`. Pada saat deklarasi, kita juga melakukan inisialisasi sekaligus dengan memberikan data `"Budi"` ke dalam variabel tadi. 

Variabel dengan tipe data String hanya menyimpan data dalam bentuk teks String, menggunakan tanda kutip ganda, silahkan perhatikan kembali tentang **Data teks** di atas. 

Akan error jika kita tidak menggunakan tanda kutip ganda dengan cara yang salah, perhatikan kode program berikut ini.

```java
public class TipeDataString {
    public static void main(String[] args) {
        
        // Inisialisasi variabel dengan tipe data String
        String nama1 = "Budi";			// Ok
        String nama2 = "Budi;			// Error
        String nama3 = Budi";			// Error
        String nama4 = Budi; 			// Error
        String nama5 = Bu"di;			// Error
        
        ...
            
    }
}
```

Penggunaan tanda kutip ganda haruslah tepat. Setiap teks harus dibuat di antara sepasang tanda kutip ganda. Begitu juga ketika ingin menggabungkan 2 (dua) String atau lebih menggunakan operator `+`. Perhatikan contoh kode program berikut.

```java
public class TipeDataString {
    public static void main(String[] args) {
        
        // Inisialisasi variabel dengan tipe data String
        String nama = "Budi";				// Teks biasa
        String tanya = "Apa " + "kabar?";	// Gabung 2 teks
        String sapa = "Hai " + nama;		// Gabung teks dan variabel 
        String kalimat = sapa + ", " + tanya; 	// Gabungan semuanya
        
        System.out.println( kalimat );
            
    }
}
```

Kode program di atas menunjukkan cara penggabungan 2 (dua) atau lebih teks menjadi data String yang benar. Perhatikan ilustrasi berikut ini.

![Struktur String](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200711062912173.png)

Begitu juga ketika kita ingin menggabungkan data String dengan variabel String ataupun dengan angka, kita perlu memperhatikan ilustrasi berikut.

![String dan Variabel](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200711063540278.png)

Perlu diingat, bahwa String hanya bisa digabung dengan String juga, atau dengan tipe data primitif. Selain itu kita tidak bisa menggabungkan data String.

### Tanda kutip tunggal dan kutip ganda

Menyimpan data teks ke dalam String harus menggunakan tanda kutip ganda, tidak boleh menggunakan tanda kutip tunggal. Penggunaan tanda kutip tunggal pada Java hanya untuk tipe data `char` saja. Perhatikan kode program berikut!

```java
public class TipeDataString {
    public static void main(String[] args) {
        
        // Error
        String nama = 'Budi';
        String tanya = 'Apa ' + 'kabar?';
        
        System.out.println( tanya );
            
    }
}
```

Semua kode program di atas tidak dapat dijalankan karena penggunaan tanda kutip tunggal untuk tipe data String. 

### Latihan memahami String

Perhatikan kode program berikut ini, identifikasi kesalahan di dalam kode program tersebut. Kemudian lakukan perbaikan sehingga mendapatkan kode program yang sesuai dengan seharusnya.

1. Kode program #1

   ```java
   public class Latihan01 {
       public static void main(String[] args) {
           
           String nama = "Budi Ja'far";
           System.out.println( nama );
               
       }
   }
   ```

   

2. Kode program #2

   ```
   public class Latihan02 {
       public static void main(String[] args) {
           
           String nama = 'Budi Ja'far';
           System.out.println( nama );
               
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class Latihan03 {
       public static void main(String[] args) {
           
           String nama = "Budi Ja'far";
           String teks = "Pada suatu hari saya melihat papan nama " + nama;
           System.out.println( teks );
               
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class Latihan04 {
       public static void main(String[] args) {
           
           String teks = "Dia berkata, \"Cepat belajar!\"";
           System.out.println( teks );
               
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class Latihan05 {
       public static void main(String[] args) {
           
           String nama = "Andi";
           String teks1 = "Saya melihat + nama + " tadi pagi.";
           String teks2 = "nama + bersama dua orang pergi pakai mobil."
           
           System.out.println( teks1 );
           System.out.println( teks2 );
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class Latihan06 {
       public static void main(String[] args) {
           
           String nama = "Andi";
           String teks1 = "Saya melihat + nama + " tadi pagi.";
           String teks2 = "nama + bersama dua orang pergi pakai mobil."
           
           System.out.println( teks1 + ". " + teks2 );
       }
   }
   ```

   


## Tipe data angka

Selain teks, tipe data angka juga merupakan tipe data yang wajib dipahami. Ada beberapa jenis tipe data angka yang dapat digunakan tergantung kebutuhan. Perhatikan kode program berikut.

```java
public class TipeDataAngka {
    public static void main(String[] args) {
        
        // Inisialisasi variabel dengan tipe data angka
        byte myByte = 2;
        short myShort = 500;
        int myInt = 20000;
        long myLong = 5000000;
        
        ...
            
    }
}
```

Menyimpan data angka pada variabel dengan tipe data angka tidak membutuhkan tanda kutip sama sekali. Cukup langsung menuliskan angka yang ingin disimpan.

Tipe data angka ada beberapa jenis, yaitu Integer (bilangan bulat), Floating point (bilangan berkoma) dan Character (karakter). Kita jelaskan satu persatu.

### Integer

Integer (bilangan bulat) adalah tipe data yang menyimpan data bilangan bulat. Ada beberapa jenis Integer di Java yaitu byte, short, int dan long. Masing-masing memiliki batas angka yang bisa disimpan.

Perhatikan tabel berikut.

| Tipe data | Size              | Range                                                       |
| --------- | ----------------- | ----------------------------------------------------------- |
| byte      | 1 byte ($2^8$)    | -128 sampai 127                                             |
| short     | 2 byte ($2^{16}$) | -32.768 sampai 32.767                                       |
| int       | 4 byte ($2^{32}$) | -2.147.483.648 sampai 2.147.483.647                         |
| long      | 8 byte ($2^{64}$) | -9.223.372.036.854.775.808 sampai 9.223.372.036.854.775.807 |

Lumayan banyak, kan? 

Kita dapat menggunakan tipe data yang sesuai dengan kebutuhan kita. Kalo angka-angka yang disimpan hanya angka kecil saja, ada baiknya kita gunakan tipe data yang lebih kecil.

### Floating Point

Floating point (bilangan berkoma) adalah tipe data khusus untuk menyimpan data bilangan pecahan atau berkoma. Floating point juga ada beberapa jenis, yaitu float dan double. Keduanya memiliki tingkat akurasi pecahan yang berbeda. Double memiliki tingkat akurasi pecahan yang bagus daripada float, jadi kalo mau melakukan perhitungan pecahan dengan tingkat ketelitian pecahan yang tinggi maka dapat menggunakan double. Perhatikan kode program berikut!

```java
public class TipeDataAngka {
    public static void main(String[] args) {
        
        float angka = 1.18f;
        double nilai = 2.15;
                   
    }
}
```

Tipe data float cukup unik karena menggunakan literal `f` di akhir data angkanya. Hal ini digunakan untuk membedakan angka float dengan angka double.

### Char

Char adalah tipe data yang menyimpan sebuah data karakter, baik angka, huruf maupun simbol. Tipe data ini hanya mampu menyimpan 1 karakter saja dalam sebuah variabel.

Kalo dilihat dari hierarkinya, tipe data char termasuk tipe data numerik. Perhatikan kode program berikut ini.

```java
public class TipeDataChar {
    public static void main(String[] args) {
        
        char x = 65;
        char y = 'A';
        
        System.out.println(x);
        System.out.println(y);
    }
}
```

Kalo kode program tersebut dijalankan, maka outputnya seperti berikut.

```shell
A
A
```

Kedua variabel x dan y sama-sama menyimpan data karakter `A`, hanya saja cara menyimpan (assignment) yang berbeda. Karakter `A` dapat disimpan menggunakan tanda kutip tunggal, juga bisa disimpan dengan memasukkan angka khusus (Unicode) tanpa tanda kutip.

### Latihan memahami tipe data angka

Perhatikan kode program berikut ini, identifikasi kesalahan di dalam kode program tersebut. Kemudian lakukan perbaikan sehingga mendapatkan kode program yang sesuai dengan seharusnya.

1. Kode program #1

   ```java
   public class Latihan01 {
       public static void main(String[] args) {
           
           byte myByte = 321;
           short myShort = 40000;
           int myInt = 2_000_000_000;
           long myLong = 0L;
           
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class Latihan02 {
       public static void main(String[] args) {
           
           byte myByte = 127;
           short myShort = 32767;
           int myInt = 2147483647;
           long myLong = 0x7fffffffffffffffL;
           
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class Latihan03 {
       public static void main(String[] args) {
           
           byte myByte = 127;
           short myShort = 32767;
           int myInt = 2147483647;
           long myLong = 0x7fffffffffffffffL;
           
           myByte = myByte + 1;
           myShort = myShort + 1;
           myInt = myInt + 1;
           myLong = myLong + 1;
   
           System.out.println(myByte);
           System.out.println(myShort);
           System.out.println(myInt);
           System.out.println(myLong);
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class Latihan04 {
       public static void main(String[] args) {
           
           byte myByte = 127;
           short myShort = 32767;
           int myInt = 2147483647;
           long myLong = 0x7fffffffffffffffL;
           
           myByte = myByte - 1;
           myShort = myShort - 1;
           myInt = myInt - 1;
           myLong = myLong - 1;
   
           System.out.println(myByte);
           System.out.println(myShort);
           System.out.println(myInt);
           System.out.println(myLong);
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class Latihan05 {
       public static void main(String[] args) {
           
           double nilai = 30/7;
           System.out.println(nilai);
           
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class Latihan06 {
       public static void main(String[] args) {
           
           int x = 30;
           int y = 7;
           double nilai = x / y;
           System.out.println(nilai);
           
       }
   }
   ```

   

7. Kode program #7

   ```java
   public class Latihan07 {
       public static void main(String[] args) {
           
           short nilai = 32767;
           System.out.println( nilai + nilai );
           
       }
   }
   ```

   

8. Kode program #8

   ```java
   public class Latihan08 {
       public static void main(String[] args) {
           
           int nilai = 2147483647 + 10;
           System.out.println( nilai + nilai );
           
       }
   }
   ```

   

## Tipe data Boolean

Boolean adalah tipe data nonnumerik yang menyimpan salah satu dari true atau false. Tipe data ini tidak bisa menyimpan data selain true atau false. Perhatikan kode program berikut!

```java
public class TipeDataBoolean {
    public static void main(String[] args) {
        
        boolean aktif = true;
        System.out.println(nilai);
        
    }
}
```

Untuk saat ini tidak banyak yang bisa kita jelaskan untuk tipe data boolean selain data `true` dan `false` saja. Pada materi berikutnya kita bakal banyak bermain-main dengan tipe boolean ini.

## Mengubah tipe data (casting)

Tipe data integer dapat diubah menjadi tipe data double, dan sebaliknya. Tetapi ada beberapa aturan yang perlu diperhatikan ketika mengubah tipe data tersebut.

### Auto casting

Perhatikan kode program berikut ini!

```java
public class AutoCasting {
    public static void main(String[] args) {
        
        // Auto casting
        short nilai = 12;
        
    }
}
```

Kode program di atas adalah contoh auto casting. Yaitu secara otomatis mengubah data integer menjadi data short. Bingung?

Secara umum, semua angka di dalam Java di anggap sebagai data int. Pada kode program di atas, angka `12` adalah data int. Sehingga proses sebenarnya adalah data int di-casting ke tipe data short. Perhatikan ilustrasi berikut!

![image-20200809075822605](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200809075822605.png)

Proses ini tidak memerlukan campur tangan programmer, Java otomatis mengenali hal ini dan akan otomatis melakukan konversi. Konsep ini cukup sederhana, apabila variabel yang digunakan cukup untuk menyimpan datanya, maka Java akan otomatis mengubah tipe data sesuai dengan variabelnya. Tapi kalo variabelnya terlalu kecil atau tidak sesuai, maka perlu dilakukan manual casting.

### Manual casting

Salah satu tujuan manual casting adalah memastikan programmer sadar tentang resiko casting. Resiko casting yang paling fatal adalah kemungkinan kehilangan angka (lossy). Contohnya seperti berikut!

```java
public class ManualCasting {
    public static void main(String[] args) {
        
        // Possible lossy
        int nilai = 25.0 / 7;
        
    }
}
```

Variabel nilai adalah int, atau bilangan bulat. Sedangkan operasi `25.0 / 7` secara default akan menghasilkan data double (berkoma). Apabila kode program ini dijalankan, Java akan memberikan pesan error bahwa konversi dari double ke int akan memiliki potensi kehilangan angka di belakang koma.

![image-20200809081534736](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200809081534736.png)

Kemungkinan kehilangan angka di belakang koma ini akan langsung diketahui oleh Java. Pada kode program ini, Java tidak mengizinkan kode tersebut dieksekusi. Kalo program tersebut dijalankan, programmer tidak akan sadar kalo hasil perhitungan bisa saja salah, dan itu sangat fatal.

Kalo programmer menyadari kemungkinan kehilangan angka (possible lossy) ini dan memang ingin tetap melanjutkan eksekusi program, maka programmer harus melakukan manual casting dengan cara mempertegas tipe data yang dihasilkan. Perhatikan kode program berikut!

```java
public class ManualCasting {
    public static void main(String[] args) {
        
        // Manual casting
        int nilai = (int) (25.0 / 7);
        
    }
}
```

Dengan demikian, Java akan tetap menjalankan kode program tadi dengan semua resikonya. Pada contoh di atas variabel `nilai` akan menyimpan angka `3` bukan `3.57`.

## Tugas

Buatlah resume tentang data, variabel dan tipe data. Jelaskan hubungan (relasi) di antara ketiga topik tersebut. Sertakan contoh-contoh kode programnya jika memungkinkan.