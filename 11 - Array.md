# Pemrograman Fundamental: Array

> Quote of the day

Array termasuk konsep dasar dalam pemrograman. Banyak kasus rumit dapat diselesaikan dengan bantuan array. Itulah mengapa array menjadi penting untuk kita pelajari.

## Konsep dasar Array

Ketika kita mendeklarasi sebuah variabel, dengan mudah kita dapat menggunakan variabel tadi pada proses berikutnya. Permasalahan semakin rumit ketika kita butuh membuat variabel dalam jumlah yang banyak. Perhatikan kode program berikut!

```java
public class KonsepArray {
    public static void main(String[] args) {
        
        int nilai = 87;
        System.out.println("Nilai = " + nilai);
        
    }
}
```

Kode program tersebut menjadi masalah ketika ada banyak variabel nilai. Misalnya nilai mahasiswa pertama, mahasiswa kedua dan seterusnya. Mungkin saja orang awam akan membuat kode program seperti berikut.

```java
public class KonsepArray {
    public static void main(String[] args) {

        int nilai1 = 87;
        int nilai2 = 69;
        int nilai3 = 81;

        System.out.println("Nilai 1 = " + nilai1);
        System.out.println("Nilai 2 = " + nilai2);
        System.out.println("Nilai 3 = " + nilai3);

    }
}
```

Tapi kode program tersebut akan semakin panjang apabila jumlah variabel nilai semakin banyak. Permasalahan ini sangat cocok jika kita menggunakan array untuk mempersingkat kode program tersebut. Perhatikan!

```java
public class KonsepArray {
    public static void main(String[] args) {

        int[] nilai = {87,69,81};

        for (int i = 0; i < nilai.length; i++) {
            System.out.println("Nilai = " + nilai[i] );
        }

    }
}
```

Kedua kode program di atas akan menghasilkan output yang sama, yaitu:

```shell
Nilai = 87
Nilai = 69
Nilai = 81
```



## Membuat Array

Sebelum menggunakan array, kita harus deklarasi array seperti mendeklarasi variabel. Hanya saja ada beberapa perbedaan ketika kita ingin melakukan deklarasi. Perhatikan kode program berikut!

```java
public class DeklarasiArray {
    public static void main(String[] args) {
		
        // Deklarasi array
        int[] angka = {2, 4, 3, 9, 4};
        for (int i = 0; i < angka.length; i++) {
            System.out.print( angka[i] + " " );
        }
    }
}
```

Berikut output yang dihasilkan.

```java
2 4 3 9 4
```



## Menggunakan Array

Array yang sudah dibuat, dapat digunakan untuk proses berikutnya dengan cara memanggil isi dari array tadi. Caranya mirip dengan menggunakan variabel, hanya saja kita harus menentukan index array yang ingin digunakan.  Perhatikan contoh kode program berikut!

```java
public class DeklarasiArray {
    public static void main(String[] args) {

        int[] angka = {2, 4, 3, 9, 4};
        System.out.println( angka[0] );
    }
}
```

Kode program di atas akan menghasilkan output,

```shell
2
```

Ini karena angka `2` berada pada indeks ke 0 pada array. Perhatikan ilustrasi array berikut!

![image-20200821092737621](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200821092737621.png)

Setiap elemen di dalam array selalu memiliki nomor indeks yang dimulai dari 0. Dengan demikian, ketika kita ingin mengakses array indeks ke 3, maka kita dapat memanggil dengan cara berikut.

```java
public class DeklarasiArray {
    public static void main(String[] args) {

        int[] angka = {2, 4, 3, 9, 4};
        System.out.println( angka[3] );
    }
}
```

Hasil kode program tersebut adalah sebagai berikut.

```java
9
```



## Memanipulasi Array

Data yang disimpan di dalam array juga dapat diubah sesuai dengan kebutuhan. Perhatikan kode program berikut ini!

```java
public class DeklarasiArray {
    public static void main(String[] args) {

        int[] angka = {2, 4, 3, 9, 4};
        
        angka[3] = 12; // manipulasi data index ke 3
        
        System.out.println( angka[3] );
    }
}
```

Kode program di atas tidak lagi menghasilkan output `9`, tetapi menghasilkan angka `12` karena sudah kita mengubah datanya. Berikut outputnya.

```java
12
```



## Duplikasi Array

Misalkan kita memiliki sebuah array dengan data-data tertentu kemudian kita buat array baru dengan data-data dari array sebelumnya. Perhatikan kode berikut!

```java
public class DeklarasiArray {
    public static void main(String[] args) {

        int[] angka = {3, 5, 6, 9, 2};
        int[] hasil = angka;

        for (int i = 0; i < hasil.length; i++) {
            System.out.print( hasil[i] + " " );
        }
        
        System.out.println();

        for (int i = 0; i < angka.length; i++) {
            System.out.print( angka[i] + " " );
        }

    }
}
```

Kode program di atas akan menghasilkan output sebagai berikut!

```shell
3 5 6 9 2
3 5 6 9 2
```

Perlu diingat, array yang sudah diduplikasi akan saling berubah ketika salah satu data di dalam array tadi kita manipulasi. Perhatikan!

```java
public class DeklarasiArray {
    public static void main(String[] args) {

        int[] angka = {3, 5, 6, 9, 2};
        int[] hasil = angka;

        hasil[3] = 15; // manipulasi

        for (int i = 0; i < hasil.length; i++) {
            System.out.print( hasil[i] + " " );
        }

        System.out.println();

        for (int i = 0; i < angka.length; i++) {
            System.out.print( angka[i] + " " );
        }

    }
}
```

Array yang dimanipulasi akan mengakibatkan array yang sama ikut berubah. Lihat output dari kode program di atas!

```shell
3 5 6 15 2 
3 5 6 15 2 
```

Kedua array yang dibuat sama-sama berubah sesuai kode program di atas.

Untuk mendapatkan duplikasi array yang sama, namun tidak saling mengubah satu sama lain adalah dengan cara membuat array seperti membuat array baru, dengan data yang sama. Perhatikan kode berikut!

```java
public class DeklarasiArray {
    public static void main(String[] args) {

        int[] angka = {3, 5, 6, 9, 2};
        int[] hasil = {3, 5, 6, 9, 2};

        hasil[3] = 15; // manipulasi

        for (int i = 0; i < hasil.length; i++) {
            System.out.print( hasil[i] + " " );
        }

        System.out.println();

        for (int i = 0; i < angka.length; i++) {
            System.out.print( angka[i] + " " );
        }

    }
}
```

Kode program ini akan menghasilkan output berikut.

```shell
3 5 6 15 2 
3 5 6 9 2 
```



## Array String

Array juga dapat dibuat dari tipe data (class) String. Perhatikan contoh berikut!

```java
public class BelajarArray {
    public static void main(String[] args) {
        
        String[] array = {"Andi", "Budi", "Citra"};
        
    }
}
```

Array String dapat digunakan, dimanipulasi dan diduplikasi seperti array lainnya. Yang membedakan hanya tipe data yang disimpan.

Perlu diingat, satu array hanya bisa menyimpan tipe data yang sama. Kali array untuk String berarti hanya bisa dipakai untuk menyimpan data String saja. Perhatikan kode program berikut!

```java
public class BelajarArray {
    public static void main(String[] args) {

        String[] array = {"Andi", "Budi", "Citra"};

        array[0] = "Alex";

        for (int i = 0; i < array.length; i++) {
            System.out.println( array[i] );
        }

    }
}
```

## Beberapa cara deklarasi array

Ada beberapa cara mendeklarasikan sebuah array, perhatikan kode berikut!

```java
public class BelajarArray {
    public static void main(String[] args) {

        // Cara umum
        int[] array = new int[5];
        
        array[0] = 62;
        array[1] = 19;
        array[2] = 21;
        array[3] = 8;
        array[4] = 46;

    }
}
```

Cara pertama ini, kita menentukan terlebih dahulu jumlah data yang disimpan di dalam array. Kode `new int[5]` menandakan kita ingin membuat array dengan jumlah 5 data yang akan disimpan.

Cara berikutnya adalah seperti pada contoh kode program kita di awal tadi. Perhatikan!

```java
public class BelajarArray {
    public static void main(String[] args) {
        
        int[] array = {62, 19, 21, 8, 46};
        
    }
}
```

Secara umum ada 2 cara tadi yang dapat kita gunakan untuk membuat sebuah array. Kita dapat memilih cara sesuai dengan yang kita butuhkan.

Namun, pola pembuatan array juga memiliki variasi, perhatikan kode program berikut!

```java
public class BelajarArray {
    public static void main(String[] args) {

        int[] angka = new int[5]; // Java-style
        int nilai[] = new int[5]; // C-style

    }
}
```

Variasi ini hanya menyangkut kenyamanan saja, mungkin ada yang sudah nyaman menggunakan cara C-style, dan ada juga yang nyaman dengan cara Java-style.

## Latihan

Perhatikan kode program berikut, kemudian jelaskan bagaimana kode program tersebut dapat berjalan!

1. Kode program #1

   ```java
   import java.util.Scanner;
   
   public class LatihanArray {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
   
           // Input jumlah data
           System.out.print("Input jumlah data = ");
           int jumlah = input.nextInt();
   
           // Buat array
           int[] nilai = new int[jumlah];
   
           // Input nilai
           for (int i = 0; i < jumlah; i++) {
               System.out.print("Nilai " + i + " = ");
               nilai[i] = input.nextInt();
           }
   
           // Output
           for (int i = 0; i < jumlah; i++) {
               System.out.print(nilai[i] + " ");
           }
   
       }
   }
   ```

   

2. Kode program #2

   ```java
   import java.util.Scanner;
   
   public class LatihanArray {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
           String[] bulan = {
                   "Januari",
                   "Februari",
                   "Maret",
                   "April",
                   "Mei",
                   "Juni",
                   "Juli",
                   "Agustus",
                   "September",
                   "Oktober",
                   "November",
                   "Desember",
           };
   
           // Input bulan
           System.out.print("Bulan ke [1-12] = ");
           int nomorBulan = input.nextInt();
   
           System.out.println( "Sekarang bulan " + bulan[nomorBulan-1] );
   
       }
   }
   ```

   

3. Kode program #3

   ```java
   import java.util.Scanner;
   
   public class LatihanArray {
       public static void main(String[] args) {
   
           Scanner input = new Scanner(System.in);
           String[] jurusan = new String[5];
           jurusan[0] = "Teknik Informatika";
           jurusan[1] = "Sistem Informasi";
           jurusan[2] = "Teknik Elektro";
           jurusan[3] = "Teknik Industri";
           jurusan[4] = "Matematika Terapan";
   
           // Pilihan
           System.out.println("Aplikasi Pilih Jurusan");
           System.out.println("======================");
           for (int i = 0; i < jurusan.length; i++) {
               System.out.print(i+1 + ". ");
               System.out.println( jurusan[i] );
           }
   
           // Input jurusan
           System.out.println("Pilih jurusan anda! ");
           System.out.print("Nomor =  ");
           int kodeJurusan = input.nextInt();
   
           System.out.println( "Selamat data di " + jurusan[kodeJurusan-1] );
   
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class LatihanArray {
       public static void main(String[] args) {
   
           int[] nilai = {31, 18, 24, 11, 42};
           
           int total = 0;
           for (int i = 0; i < nilai.length; i++) {
               total += nilai[i];
           }
   
           System.out.println("Total = " + total);
   
       }
   }
   ```

   

5. Kode program #5

   ```java
   import java.util.Arrays;
   
   public class LatihanArray {
       public static void main(String[] args) {
   
           String[] buah = {
                   "Mangga",
                   "Jeruk",
                   "Apel",
                   "Semangka",
           };
   
           Arrays.sort(buah);
   
           for (int i = 0; i < buah.length; i++) {
               System.out.println( (i+1) + ". " + buah[i]);
           }
   
       }
   }
   ```

   

## Array Multidimensi

Array multidimensi sederhananya adalah array yang menyimpan data array juga. Pada array 1 dimensi kita dapat mengilustrasikan array tersebut seperti pada gambar berikut.

![image-20200821092737621](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200821092737621.png)

Sedangkan pada array 2 dimensi, ilustrasi array menjadi seperti berikut.

![image-20200919220712735](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200919220712735.png)

Dari ilustrasi di atas dapat dilihat bahwa kita memiliki array yang di dalam masing-masing datanya menyimpan array juga. Sehingga cara pemanggilan data di dalam array multidimensi juga ada sedikit perbedaan. Perhatikan kode program berikut!

```java
public class LatihanArray {
    public static void main(String[] args) {

        // Deklarasi array multidimensi
        int[][] data = {
                {2, 4, 3, 9, 4},
                {3, 5, 4, 0, 3},
                {4, 6, 5, 1, 6},
        };

        // Cetak data indeks 1,3
        System.out.println( data[1][3] );

    }
}
```

## Beberapa cara deklarasi array multidimensi

Sama seperti deklarasi array 1 dimensi, deklarasi array multidimensi dapat menggunakan berbagai cara. Perhatikan kode program berikut!

```java
public class LatihanArray {
    public static void main(String[] args) {

        // Deklarasi array multidimensi
        int[][] data = {
                {2, 4, 3, 9, 4},
                {3, 5, 4, 0, 3},
                {4, 6, 5, 1, 6},
        };

    }
}
```

Cara pertama, langsung input value dari array-nya. Mirip seperti array 1 dimensi. Cukup sederhana dan mudah dibuat. Berbeda dengan cara berikutnya.

```java
public class LatihanArray {
    public static void main(String[] args) {

        // Deklarasi array multidimensi
        int[][] data = new int[3][5];
        
        data[0][0] = 2;
        data[0][1] = 4;
        data[0][2] = 3;
        data[0][3] = 9;
        data[0][4] = 4;
        
        data[1][0] = 2;
        data[1][1] = 4;
        data[1][2] = 3;
        data[1][3] = 9;
        data[1][4] = 4;
        
        data[2][0] = 2;
        data[2][1] = 4;
        data[2][2] = 3;
        data[2][3] = 9;
        data[2][4] = 4;
        
    }
}
```

Cara kedua, sangat sederhana namun sangat panjang sekali. Kita menentukan satu persatu value yang ada di dalam array. 

## Tugas

