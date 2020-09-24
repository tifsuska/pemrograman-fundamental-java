# Pemrograman Fundamental: Expression, Statement dan Block

> Quote of the day

Menulis sebuah kode program tidak bisa sekedar meniru kode program orang lain dan banyak latihan. Bisa-bisa kita akan menghabiskan banyak waktu namun hasil kurang maksimal.

Mulailah memahami hal dasar sekali. Kemudian kenali komponen-komponen pembentukan kode program sehingga kita bisa lebih paham dan lebih bebas berinovasi.

Komponen dasar dalam menulis sebuah kode program di Java adalah expression, statement dan block. Pada materi ini kita akan membahas tentang ketiga komponen tersebut.

## Expression

Sebuah expression terdiri dari data, variabel dan atau operator. Supaya mudah memahaminya, perhatikan kode program berikut ini!

```java
public class Expression {
    public static void main(String[] args) {

        int nilai = 10;
        nilai = nilai + 5;
        System.out.println("Nilai = " + nilai);

    }
}
```

Dari kode program di atas kita akan identifikasi yang mana yang namanya expression. Perhatikan ilustrasi berikut!

![image-20200816232216230](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200816232216230.png)

Data angka `10` adalah expression, karena itu adalah data, berbentuk angka dengan nilai `10`. Kita coba dengan ilustrasi berikutnya, perhatikan!

![image-20200816232450875](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200816232450875.png)

Kode `nilai = 10` juga adalah expression, selama tidak kita masukkan tanda `;` (titik-koma) maka kode tersebut adalah expression. 

Perhatikan lagi ilustrasi berikut ini!

![image-20200816233600470](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200816233600470.png)

Pada kode program di atas, kode `5` dan `nilai + 5` dan `nilai = nilai + 5` adalah expression, selama tidak memasukkan tanda `;` (titik-koma).

Penting bagi kita untuk memahami dan membuat sebuah expression di dalam Java. Bentuk expression ini juga dapat digunakan pada bahasa pemrograman lainnya.

Berikut ini merupakan beberapa jenis expression yang ada dalam Java.

```java
public class Expression {
    public static void main(String[] args) {

        // data expression + assignment expression
        int nilai = 10;
        String nama = "Andi";
        String teks = "Hai " + nama;

    }
}
```

Data angka `10` atau `"Andi"` atau `"Hai " + nama` adalah data expression dalam bentuk data. Sedangkan `nilai = 10` atau `nama = "Andi"` atau `teks = "Hai " + nama` adalah assignment expression.

```java
public class Expression {
    public static void main(String[] args) {

        int nilai = 10;
        
        // Unary expression
        nilai++;
        ++nilai;
        
        // Object creation expression
        Scanner scn = new Scanner(System.in);
        
        // Method invocation expression
        System.out.println( nilai );

    }
}
```

Kode `nilai++` atau `++nilai` adalah unary expression dan `Scanner scn = new Scanner()` adalah object creation expression. Sedangkan `System.out.println()` adalah method invocation expression. Perlu diperhatikan, bahwa semua expression tidak mengikutsertakan tanda `;` (titik-koma) di akhirnya.

### Latihan memahami expression

Perhatikan kode program berikut, kemudian identifikasi kode yang merupakan expression.

1. Kode program #1

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           int x = 10, y = 11, z = 12;
           System.out.println( x + y + z );
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           int x = 10, y = 11, z = 12;
           x = y + z;
           y = x + z;
           z = y + z;
           System.out.println( x + y + z );
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           String nama = "Affandes";
           System.out.println( "Hai " + nama );
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           String nama = "Affandes";
           System.out.printf( "Hai %s (%d)", nama, nama.length() );
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           String nama = "Affandes";
           String teks = "Hai ";
           System.out.println( teks + nama.substring(0, 5));
       }
   }
   ```

   

## Statement

Di dalam bahasa manusia ada istilah kata, dan kalimat. Maka di dalam Java dan bahasa pemrograman, statement adalah kalimatnya. Kalimat biasanya diakhiri dengan tanda titik, sedangkan statement diakhiri dengan tanda `;` (titik-koma).

Perhatikan kode program berikut ini!

```java
public class Statement {
    public static void main(String[] args) {

        // Statement
        int nilai = 10;
        
        // Statement
        nilai++;
        ++nilai;
        
        // Statement
        System.out.println( nilai );

    }
}
```

Setiap expression yang diakhiri dengan tanda `;` (titik-koma) adalah statement. Fix, simple! 

Tapi, selain itu ada juga statement lain, yaitu control flow statement. Control flow statement terdiri dari 2 (dua) jenis, yaitu:

1. Branching, adalah percabangan menggunakan if-else dan switch-case.
2. Looping, adalah perulangan menggunakan for, while dan do-while.

Kedua topik ini akan kita bahas pada bab terpisah, yaitu Bab 09 dan Bab 10.

### Latihan memahami statement

Perhatikan kode program berikut, kemudian identifikasi jenis statement pada kode program tersebut!

1. Kode program #1

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           int x = 10, y = 11, z = 12;
           System.out.println( x + y + z );
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           int x = 10, y = 11, z = 12;
           x = y + z;
           y = x + z;
           z = y + z;
           System.out.println( x + y + z );
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           String nama = "Affandes";
           System.out.println( "Hai " + nama );
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           String nama = "Affandes";
           System.out.printf( "Hai %s (%d)", nama, nama.length() );
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           String nama = "Affandes";
           String teks = "Hai ";
           System.out.println( teks + nama.substring(0, 5));
       }
   }
   ```

   

## Block 

Block (blok) adalah cara sederhana mengelompokkan statement ke dalam tanda kurung kurawal `{}` untuk kebutuhan tertentu. Perhatikan contoh kode program berikut!

```java
public class Statement {
    public static void main(String[] args) {

        int nilai = 10;

        {				// Blok
            int x = 5;
            nilai += x;
        }				// akhir blok

        System.out.println("Nilai = " + nilai);
		System.out.println("X = " + x);		// Error
        
    }
}
```

Perlu dipahami bahwa penggunaan blok akan mempengaruhi scope dari variabel. Perhatikan kode di atas! Kode `int nilai = 10;` adalah deklarasi variabel global. Dapat digunakan selama di dalam psvm. Sedangkan kode `int x = 5;` adalah deklarasi variabel lokal, hanya dapat digunakan di dalam blok itu saja. Tidak dapat digunakan di luar blok.

### Latihan memahami block

Perhatikan kode program berikut, kemudian jelaskan bagaimana program tersebut dapat berjalan!

1. Kode program #1

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
           
           {
               int nilai = 10;
               System.out.println( nilai );
           }
   
           System.out.println( nilai );
           
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
   
           int nilai = 19;
           
           {
               System.out.println( nilai );
           }
   
           System.out.println( nilai );
   
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class BelajarExpression {
       public static void main(String[] args) {
   
           {
               int nilai = 10;
               System.out.println( nilai );
           }
           
           {
               int nilai = 9;
               System.out.println( nilai );
           }
   
       }
   }
   ```

   

## Tugas