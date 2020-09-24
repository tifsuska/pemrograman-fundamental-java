# Pemrograman Fundamental: Perulangan

> Quote of the day

Salah satu kelebihan komputer adalah dapat melakukan kalkulasi dengan akurat dan cepat. Proses yang cepat ini menjadikan komputer mampu melakukan kalkulasi tepat dalam jumlah yang banyak sekali. Untuk melakukan itu, dibutuhkan perulangan.

## Konsep dasar perulangan

Sebagian besar proses di dalam program adalah perulangan. Proses yang sama diulang-ulang sekian banyak sesuai dengan kebutuhan. Namun secara prinsip, sebuah perulangan memiliki setidaknya beberapa hal penting, yaitu:

1. Posisi awal
Setiap perulangan harus dimulai dari posisi tertentu, ini disebut posisi awal. Misalnya ulang dari 1 sampai sekian. Angka 1 adalah posisi awal perulangan.
   
2. Kondisi
Kita perlu tahu kondisi seperti apa yang memicu perulangan terus berjalan atau berhenti. Misalnya ketika nilai masih kurang dari 100, maka ulangi lagi.
   
3. Proses
Untuk apa melakukan perulangan jika tidak ada apa-apa. Harusnya ada proses-proses yang akan diulangi.
   
4. Perubahan (update)
Perulangan bukan berarti sama secara keseluruhan. Ada data dan nilai tertentu yang harus berubah mendekati titik akhir perulangan. Jangan sampai kalkulasi bermasalah sehingga proses perulangan tidak berhenti.

Dengan adanya keempat hal tersebut, dalam implementasinya kita harus mampu mengidentifikasi keempatnya.

## Perulangan dalam bentuk flowchart

Sebenarnya flowchart tidak punya diagram khusus untuk perulangan. Di dalam pembuatan flowchart, perulangan dikonversi menjadi percabangan. Perhatikan diagram berikut ini!

![image-20200821054139263](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200821054139263.png)

Jika diperhatikan flowchart tersebut, lengkap ada 4 komponen penting di dalam sebuah perulangan, yaitu:

1. Posisi awal, adalah diagram pertama `nilai awal = 1`
2. Kondisi, adalah diagram berikutnya `nilai < 10`
3. Proses, adalah diagram jika kondisi ya, `Output "Salam"`
4. Perubahan, adalah diagram yang mengubah nilai, `nilai = nilai + 1`

Penggunaan pola flowchart seperti ini lebih mudah dipahami, sehingga memudahkan pada saat implementasi ke dalam bahasa pemrograman Java.

## For

Salah satu implementasi perulangan menggunakan bahasa pemrograman Java adalah menggunakan statement for. Perhatikan contoh penggunaannya!

```java
public class SimpelFor {
    public static void main(String[] args) {
        
        for (int nilai = 1; nilai < 10; nilai++) {
            System.out.println("Salam");
        }
        
    }
}
```

Kode program tersebut dibuat berdasarkan flowchart yang sudah kita buat sebelumnya. Silahkan lakukan perbandingan terhadap kode program dan flowchart tersebut.

Kode program di atas akan menghasilkan output seperti berikut.

```shell
Salam
Salam
Salam
Salam
Salam
Salam
Salam
Salam
Salam
```

Kode program tersebut dapat kita modifikasi sesuai dengan kebutuhan. Misalnya kita ingin menampilkan tulisan `Salam` sebanyak 100 kali, kita tinggal mengatur bagian kondisinya.

Umumnya statement for dapat ditulis dengan singkat seperti kode program berikut ini.

```java
public class SimpelFor {
    public static void main(String[] args) {
        
        for (int i = 1; i < 10; i++) {
            System.out.println("Salam");
        }
        
    }
}
```

## While

Selain for,  statement while dapat digunakan untuk melakukan perulangan. Perhatikan kode program berikut!

```java
public class SimpelWhile {
    public static void main(String[] args) {

        int i = 1;
        while ( i < 10 ) {
            System.out.println("Salam");
            i++;
        }

    }
}
```

Kode program tersebut akan menghasilkan output yang sama dengan kode program sebelumnya.

Antara for dan while secara sintak memang berbeda, tapi konsep perulangannya tetap sama. Keduanya sama-sama memiliki 4 komponen penting dalam perulangan. Silahkan identifikasi keempat komponen penting dalam perulangan yang ada di dalam statement while.

## Do while

Statement while dan do-while sebenarnya juga sama. Mereka memiliki 4 komponen penting dalam sebuah perulangan. Perhatikan contoh kode program berikut!

```java
public class SimpelWhile {
    public static void main(String[] args) {

        int i = 1;
        do {
            System.out.println("Salam");
            i++;
        } while ( i < 10 );

    }
}
```

Yang membedakannya adalah posisi while diletakkan di bagian akhir. Akibatnya, kode program yang ada di dalam blok proses pasti akan dijalankan minimal 1 kali, walaupun kondisi bernilai negatif/false.

## Latihan

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut dapat menghasilkan outputnya!

1. Kode program #1

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 10; i++) {
               System.out.println( i );
           }
   
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 10; i++) {
               System.out.print( i );
           }
   
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 10; i++) {
               System.out.print( i+10 + " " );
           }
   
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 20; i += 2) {
               System.out.println( "Step " + (i+1) );
           }
   
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 10; i > 0; i--) {
               System.out.println( "Step " + (i * 2) );
           }
   
       }
   }
   ```

   

## Nested block

Lagi-lagi karena for dan while termasuk control flow statement, maka sangat memungkinkan untuk menggunakan percabangan dan perulangan di dalam for dan while. 

Semakin banyak perulangan yang dibuat, semakin kompleks proses yang ada di dalam program kita. Hal ini perlu diperhatikan untuk menghindari proses perulangan yang sangat banyak atau bahkan perulangan yang tiada henti (infinity).

Berikut contoh penggunaan nested for.

```java
public class SimpelWhile {
    public static void main(String[] args) {

        for (int i = 0; i < 10; i++) {
            for (int j = 0; j < 10; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }

    }
}
```

Kode program di atas akan menghasilkan output seperti berikut.

```shell
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
0 1 2 3 4 5 6 7 8 9 
```

### Latihan

Perhatikan kode program berikut, kemudian jelaskan bagaimana kode program tersebut dapat berjalan!

1. Kode program #1

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 5; i++) {
               for (int j = 0; j < 3; j++) {
                   System.out.println(i);
               }
           }
   
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 5; i++) {
               for (int j = 0; j < 3; j++) {
                   System.out.println(i);
               }
           }
   
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 5; i++) {
               for (int j = 0; j < 3; j++) {
                   System.out.println("Cetak j = " + j);
               }
               System.out.println("Print i = " + i);
               System.out.println();
           }
   
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 5; i++) {
               System.out.println("Print i = " + i);
               for (int j = 4; j > 0; j--) {
                   System.out.println("Cetak j = " + j);
               }
               System.out.println();
           }
   
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 5; i++) {
               for (int j = 4; j > 0; j--) {
                   System.out.print("o");
               }
               System.out.println("x");
           }
   
       }
   }
   ```

6. Kode program #6

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 5; i++) {
               for (int j = 4; j > 0; j--) {
                   if (j > 2) {
                       System.out.print("o");
                   } else {
                       System.out.print("x");
                   }
               }
               System.out.println();
           }
   
       }
   }
   ```

   

7. Kode program #7

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 5; i++) {
               for (int j = 4; j > 0; j--) {
                   if (i > 2) {
                       System.out.print("o");
                   } else {
                       System.out.print("x");
                   }
               }
               System.out.println();
           }
   
       }
   }
   ```

   

8. Kode program #8

   ```java
   public class BelajarLoop {
       public static void main(String[] args) {
   
           for (int i = 0; i < 5; i++) {
               for (int j = 4; j > 0; j--) {
                   if (i < 2) {
                       System.out.print("o");
                   } else {
                       System.out.print(j);
                   }
               }
               System.out.println();
           }
   
       }
   }
   ```

   

## Tugas