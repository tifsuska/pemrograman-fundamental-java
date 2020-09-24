# Programming Fundamentals: Operator

> Quote of the day

Data dan variabel tidak akan berguna jika tidak dioperasikan. Operasi data dan variabel sangat banyak sekali. Misalkan menambahkan antara variabel pertama dan variabel kedua, dan sebagainya.

Itulah mengapa kita perlu memahami tentang fundamental dari Operator pada Pemrograman Java. Materi kali ini bakal kita bahas tuntas tentang berbagai jenis operator pada Java.

## Operator dan Operand

Ada 2 (dua) istilah yang harus kita pahami pada awal pembahasan ini, yaitu Operator dan Operand. Operator adalah simbol yang berfungsi untuk menjalankan operasi. Sedangkan operand adalah data atau variabel atau lainnya yang dioperasikan.

### Kenali yang mana operator dan operand

Kenali operator dan operand yang ada di dalam kode program. Perhatikan cuplikan kode program berikut ini!

![image-20200816091520808](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200816091520808.png)

Tanda ➕ pada ilustrasi di atas adalah sebuah operator. Sedangkan angka 10 dan angka 25 adalah operand. Ketika operator dijalankan terhadap operand, maka operator tersebut akan menghasilkan sebuah data baru. Pada contoh di atas, angka `10` ditambahkan dengan angka `25` akan menghasilkan angka baru, yaitu angka `35` dengan tipe data `int`. 

Selain tanda ➕ operator juga terdapat banyak simbol lainnya yang berfungsi sebagai operator. Mengetahui berbagai macam operator akan memudahkan kita untuk membuat sebuah instruksi pada pemrograman Java. Perhatikan kode program berikut ini!

```java
public class Operator {
    public static void main(String[] args) {

        int nilai = 10;				// baris ke 4
        int hasil = nilai + 20;		// baris ke 5

    }
}
```

Pada baris ke 4 kode program di atas, simbol `=` (sama dengan) adalah juga operator. Simbol tersebut berfungsi untuk menyimpan data yang ada pada operand sebelah kanan, disimpan ke operand sebelah kiri.

Pada baris ke 5 kode program di atas terdapat 2 (dua) operator yang berbeda, yaitu operator `=` dan operator `+`. Kedua operator ini akan dioperasikan berurutan sesuai dengan ketentuan tertentu. Perhatikan ilustrasi berikut!

![image-20200816095056011](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200816095056011.png)

Apabila terdapat beberapa operator dalam satu instruksi, maka setiap operator akan diproses sesuai dengan ketentuan dan tingkat prioritas dari masing-masing operator. Ketentuan ini disebut dengan precedence (lihat pada subbab terakhir).

Pada contoh ilustrasi di atas, operator yang dijalankan terlebih dahulu adalah operator `+` yaitu menambahkan data pada variabel `nilai` ditambahkan dengan angka `20` sehingga menjadi angka `30`. Selanjutnya baru dijalankan operator `=` untuk menyimpan angka `30` tadi ke dalam variabel `hasil`. 

Berbeda operator, berbeda pula tingkat prioritasnya. Kita akan bahas materi ini pada subbagian **Operator Precedence** pada pemrograman Java.

### Latihan memahami operator dan operand

Perhatikan kode program berikut, kenali bagian kode program tersebut dan tentukan yang manakah operator dan manakah operand. 

1. Kode program #1

   ```java
   public class Latihan01 {
       public static void main(String[] args) {
   
           int nilai;
           nilai = 19;
           
           int angka = 10, bilangan = 13, nomor = 15;
   
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class Latihan02 {
       public static void main(String[] args) {
   
           String nama = "Andi";
           String pesan = "Hai " + nama + ". Apa kabar?";
           String doa = "Semoga hari ini lebih baik dari kemarin";
           String kalimat = pesan + ". " + doa;
   
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class Latihan03 {
       public static void main(String[] args) {
   
           int x = 10;
           int y = 15;
           int hasil = x + y / 5;
   
       }
   }
   ```

   

## Operator Assignment, Aritmetic dan Unary

Pada subbagian ini kita akan menjelaskan tentang beberapa jenis operator yang paling sering digunakan pada pemrograman Java, yaitu operator assignment, operator aritmatika dan operator unary.

### Operator Assignment

Operator yang paling sering adalah operator assignment, yaitu simbol `=` (sama dengan). Operator ini berfungsi untuk menyalin atau menyimpan data ke dalam sebuah variabel. Data yang disimpan adalah operand sebelah kanan, sedangkan variabel tempat menyimpan adalah operand sebelah kiri.

![image-20200816102424343](https://raw.githubusercontent.com/tifsuska/pemrograman-fundamental-java/master/assets/image-20200816102424343.png)

Operator ini hanya ada satu saja, yaitu `=` (sama dengan).

| No   | Simbol | Contoh | Deskripsi                           |
| ---- | ------ | ------ | ----------------------------------- |
| 1    | =      | x = y  | Menyimpan nilai y ke variabel x     |
| 2    | +=     | x += y | Menyimpan nilai x + y ke variabel x |
| 3    | -=     | x -= y | Menyimpan nilai x - y ke variabel x |
| 4    | *=     | x *= y | Menyimpan nilai x * y ke variabel x |
| 5    | /=     | x /= y | Menyimpan nilai x / y ke variabel x |
| 6    | %=     | x %= y | Menyimpan nilai x % y ke variabel x |



### Operator Aritmetic

Operator lainnya yang paling sering digunakan dalam pemrograman adalah operator aritmatika. 

| No   | Simbol | Contoh | Deskripsi                       |
| ---- | ------ | ------ | ------------------------------- |
| 1    | +      | x + y  | Menghitung hasil x ditambah y   |
| 2    | -      | x - y  | Menghitung hasil x dikurang y   |
| 3    | *      | x * y  | Menghitung hasil x dikali y     |
| 4    | /      | x / y  | Menghitung hasil x dibagi y     |
| 5    | %      | x % y  | Menghitung sisa bagi x dibagi y |



### Operator Unary

Operator unary adalah operator yang hanya butuh 1 (satu) operand saja. Operator unary ada yang memiliki operand di sebelah kanan saja, ada juga memiliki operand di sebelah kiri atau di sebelah kanan.

Berikut ini adalah operator unary yang memiliki operand di sebelah kanan saja.

| No   | Simbol | Contoh | Deskripsi                               |
| ---- | ------ | ------ | --------------------------------------- |
| 1    | +      | +12    | Menyatakan angka positif                |
| 2    | -      | -20    | Menjadikan angka negatif                |
| 3    | !      | !false | Komplemen atau membalikkan nilai logika |

Berikut ini adalah operator unary yang memiliki operand di sebelah kiri atau di sebelah kanan.

| No   | Simbol | Contoh       | Deskripsi           |
| ---- | ------ | ------------ | ------------------- |
| 1    | ++     | ++x atau x++ | Menambahkan angka 1 |
| 2    | --     | --x atau x-- | Mengurangi angka 1  |

Simbol `++` dan `--` juga disebut dengan operator increment dan operator decrement. Operator yang diletakkan sebelum operand (pre-increment) dengan operator yang diletakkan setelah operand memiliki operasi yang sedikit berbeda.

Perhatikan kode program berikut ini!

```java
public class Operator {
    public static void main(String[] args) {

        int x = 10;
        int y = x++;			// post-increment
        System.out.println(x);
        System.out.println(y);

    }
}
```

Kode program di atas akan menghasilkan output seperti berikut.

```shell
11
10
```

Sedangkan kode program berikut

```java
public class Operator {
    public static void main(String[] args) {

        int x = 10;
        int y = ++x;			// pre-increment
        System.out.println(x);
        System.out.println(y);

    }
}
```

akan menghasilkan output berikut

```shell
11
11
```

Pada **pre-increment** nilai `x` sudah ditambahkan dengan `1` menjadi angka `11` setelah itu baru disimpan ke variabel `y`. Sedangkan pada **post-increment** nilai `x` belum ditambahkan dengan `1` sehingga angkanya masih `10`, angka `10` tadi disimpan ke variabel `y`, setelah itu baru ditambahkan `1` menjadi `11`.

### Latihan memahami operator assignment

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut jika dijalankan. 

1. Kode program #1

   ```java
   public class BelajarAssign {
       public static void main(String[] args) {
           
           int nilai = 10;
           nilai = 11;
           System.out.println(nilai);
           
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class BelajarAssign {
       public static void main(String[] args) {
   
           int nilai = 10;
           nilai = nilai + 1;
           System.out.println(nilai);
   
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class BelajarAssign {
       public static void main(String[] args) {
   
           int nilai = 10;
           nilai + 1;
           System.out.println(nilai);
   
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class BelajarAssign {
       public static void main(String[] args) {
   
           int nilai;
           System.out.println(nilai);
   
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class BelajarAssign {
       public static void main(String[] args) {
   
           int a = 10;
           int b = 11;
           int c = 12;
   
           a += 5;
           b *= 5;
           c %= 5;
   
           System.out.println(a);
           System.out.println(b);
           System.out.println(c);
   
       }
   }
   ```

   

### Latihan memahami operator aritmetic

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut jika dijalankan. 

1. Kode program #1

   ```java
   public class OpAritmatika {
       public static void main(String[] args) {
           int x = 10;
           int y = 15;
           int z = 18;
           System.out.println( x + y - z );
           System.out.println( x * y - z );
           System.out.println( x + y / z );
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class OpAritmatika {
       public static void main(String[] args) {
           int x = 10, y = 15, z = 5;
           int a = (x + y) / z;
           int b = x * (y + z);
           int c = x + y % z;
           System.out.println(a);
           System.out.println(b);
           System.out.println(c);
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class OpAritmatika {
       public static void main(String[] args) {
           int x = 10, y = 15, z = 5;
           int hasil = y / (x % z);
           System.out.println(hasil);
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class OpAritmatika {
       public static void main(String[] args) {
           System.out.println( 10 + 2 + 5 * 10 );
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class OpAritmatika {
       public static void main(String[] args) {
           System.out.println( "Hasil = " + 10 + 2 + 5 * 10 );
       }
   }
   ```

   

### Latihan memahami operator unary

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut jika dijalankan. 

1. Kode program #1 

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           System.out.println( +10 );
           System.out.println( -10 );
           System.out.println( !true );
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           int a = -10;
           int b = +10;
           int c = +a +b -5;
           System.out.println(a);
           System.out.println(b);
           System.out.println(c);
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           int a = -10;
           int b = +10;
           int c = +a + -b -5;
           System.out.println(a);
           System.out.println(b);
           System.out.println(c);
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           int a = 10;
           a++;
           System.out.println(a);
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           int a = 10;
           System.out.println( a++ );
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           int a = 10;
           System.out.println( ++a );
       }
   }
   ```

   

7. Kode program #7

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           int a = 10;
           int b = 15;
   
           System.out.println( a++ + ++b );
           System.out.println( a );
           System.out.println( b );
       }
   }
   ```

   

8. Kode program #8

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           int a = 10;
           int b = 15;
   
           System.out.println( a++ + ++b );
           System.out.println( a++ + ++b );
           System.out.println( a );
           System.out.println( b );
       }
   }
   ```

   

9. Kode program #9

   ```java
   public class OpUnary {
       public static void main(String[] args) {
           int a = 10;
           int b = 15;
   
           System.out.println( ++a+ ++b );
           System.out.println( --a- --b );
           System.out.println( a );
           System.out.println( b );
       }
   }
   ```

   

10. Kode program #10

    ```java
    public class OpUnary {
        public static void main(String[] args) {
            int a = 10;
            System.out.println( a++ + ++a );
            System.out.println( a );
        }
    }
    ```

    



## Operator Equality, Relational dan Conditional

Yang menarik dari ketiga operator ini adalah semua operatornya akan menghasilkan tipe data boolean (true atau false). 

### Operator Equality

Berikut adalah operator equality

| No   | Simbol | Contoh | Deskripsi                                     |
| ---- | ------ | ------ | --------------------------------------------- |
| 1    | ==     | x == y | Menghasilkan **true** jika x sama dengan y    |
| 2    | !=     | x != y | Menghasilkan **true** jika x berbeda dengan y |

### Operator Relational

Berikut adalah operator relational

| No   | Simbol | Contoh | Deskripsi                                                   |
| ---- | ------ | ------ | ----------------------------------------------------------- |
| 1    | >      | x > y  | Menghasilkan **true** jika x lebih besar dari y             |
| 2    | <      | x < y  | Menghasilkan **true** jika x lebih kecil dari y             |
| 3    | >=     | x >= y | Menghasilkan **true** jika x lebih besar atau sama dengan y |
| 4    | <=     | x <= y | Menghasilkan **true** jika x lebih kecil atau sama dengan y |

### Operator Conditional

Berikut adalah operator conditional. Perlu diperhatikan, tipe data operand pada operator ini adalah boolean.

| No   | Simbol | Contoh   | Deskripsi         |
| ---- | ------ | -------- | ----------------- |
| 1    | &      | x & y    | Logika AND        |
| 2    | &&     | x && y   | Short circuit AND |
| 3    | \|     | x \| y   | Logika OR         |
| 4    | \|\|   | x \|\| y | Short circuit OR  |
| 5    | ^      | x ^ y    | Logika XOR        |

Untuk memahami tentang logika AND silahkan pahami tabel logika berikut!

| Nilai X | Nilai Y | Hasil AND |
| ------- | ------- | --------- |
| true    | true    | true      |
| true    | false   | false     |
| false   | true    | false     |
| false   | false   | false     |

Untuk memahami tentang logika OR silahkan pahami tabel logika berikut!

| Nilai X | Nilai Y | Hasil OR |
| ------- | ------- | -------- |
| true    | true    | true     |
| true    | false   | true     |
| false   | true    | true     |
| false   | false   | false    |

Untuk memahami tentang logika XOR silahkan pahami tabel logika berikut!

| Nilai X | Nilai Y | Hasil XOR |
| ------- | ------- | --------- |
| true    | true    | false     |
| true    | false   | true      |
| false   | true    | true      |
| false   | false   | false     |

Biar mudah mengetahui logika AND, OR dan XOR berikut best practices nya:

1. Logika AND akan menghasilkan **true** jika x dan y juga **true**.
2. Logika OR akan menghasilkan **false** jika x dan y juga **false**.
3. Logika XOR akan menghasilkan **true** jika x dan y **berbeda**.



### Latihan memahami operator equality

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut jika dijalankan. 

1. Kode program #1 

   ```java
   public class OpEquality {
       public static void main(String[] args) {
           int x = 10;
           int y = 10;
           System.out.println( x==y );
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class OpEquality {
       public static void main(String[] args) {
           int x = 10;
           int y = 11;
           System.out.println( x==y-1 );
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class OpEquality {
       public static void main(String[] args) {
           int x = 10;
           int y = 11;
   
           boolean z = y - x == 1;
           System.out.println( z );
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class OpEquality {
       public static void main(String[] args) {
           int x = 10;
           int y = 11;
           int z = y - x;
   
           System.out.println( z != 1 );
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class OpEquality {
       public static void main(String[] args) {
           int x = 10;
           int y = 11;
   
           boolean z = x - y != y - x;
           System.out.println( z );
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class OpEquality {
       public static void main(String[] args) {
           int x = 10;
   
           boolean z = x == x++;
           System.out.println( z );
       }
   }
   ```

   

### Latihan memahami operator relaional

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut jika dijalankan. 

1. Kode program #1 

   ```java
   public class OpRelation {
       public static void main(String[] args) {
           int nilai = 10;
           int angka = 11;
           System.out.println( nilai > angka );
           System.out.println( nilai < angka );
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class OpRelation {
       public static void main(String[] args) {
           int nilai = 10;
           int angka = 11;
   
           System.out.println( nilai+1 >= angka );
           System.out.println( nilai+1 <= angka );
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class OpRelation {
       public static void main(String[] args) {
           int nilai = 10;
           int angka = 11;
   
           System.out.println( nilai++ >= angka );
           System.out.println( nilai-- <= angka );
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class OpRelation {
       public static void main(String[] args) {
           int x = 5;
           int y = 8;
   
           boolean hasil1 = (2 * x) > y;
           boolean hasil2 = x + y < x + x;
           boolean hasil3 = x % 4 >= y % 4;
   
           System.out.println(hasil1);
           System.out.println(hasil2);
           System.out.println(hasil3);
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class OpRelation {
       public static void main(String[] args) {
           int x = 5;
           int y = 8;
   
           boolean hasil1 = (2 * x++) > y--;
           boolean hasil2 = x++ + --y < x + x;
           boolean hasil3 = x % 4 >= y % 4;
   
           System.out.println(hasil1);
           System.out.println(hasil2);
           System.out.println(hasil3);
       }
   }
   ```

   

### Latihan memahami operator conditional

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut jika dijalankan. 

1. Kode program #1 

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           boolean satu = true;
           boolean dua = false;
           
           boolean hasil1 = satu & dua;
           boolean hasil2 = satu | dua;
   
           System.out.println(hasil1);
           System.out.println(hasil2);
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           int x = 5;
           int y = 8;
   
           boolean satu = x < y;
           boolean dua = x > y;
   
           boolean hasil1 = satu & dua;
           boolean hasil2 = satu | dua;
   
           System.out.println(hasil1);
           System.out.println(hasil2);
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           int x = 5;
           int y = 8;
   
           boolean satu = x + 2 <= y - 1;
           boolean dua = x + y > y + y;
   
           boolean hasil1 = satu & dua;
           boolean hasil2 = satu | dua;
   
           System.out.println(hasil1);
           System.out.println(hasil2);
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           int x = 5;
           int y = 8;
   
           boolean hasil1 = x + 2 <= y - 1 & x + y > y + y;
           boolean hasil2 = x + 2 <= y - 1 | x + y > y + y;
   
           System.out.println(hasil1);
           System.out.println(hasil2);
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           int a = 5;
           int b = 12;
   
           boolean hasil = a++ >= 6 & b++ < 15;
   
           System.out.println(a);
           System.out.println(b);
           System.out.println(hasil);
       }
   }
   ```

   

6. Kode program #6

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           int a = 5;
           int b = 12;
   
           boolean hasil = a++ >= 6 && b++ < 15;
   
           System.out.println(a);
           System.out.println(b);
           System.out.println(hasil);
       }
   }
   ```

   

7. Kode program #7

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           int a = 5;
           int b = 12;
   
           boolean hasil = a++ < 6 | b++ < 15;
   
           System.out.println(a);
           System.out.println(b);
           System.out.println(hasil);
       }
   }
   ```

   

8. Kode program #8

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           int a = 5;
           int b = 12;
   
           boolean hasil = a++ < 6 || b++ < 15;
   
           System.out.println(a);
           System.out.println(b);
           System.out.println(hasil);
       }
   }
   ```

   

9. Kode program #9

   ```java
   public class OpConditional {
       public static void main(String[] args) {
           int a = 5;
           int b = 12;
   
           boolean hasil = a == a ^ b != b;
           System.out.println(hasil);
       }
   }
   ```

   


## Operator Bitwise dan Bit Shift

Kedua operator ini sangat jarang sekali digunakan dalam pemrograman. Hanya kasus-kasus khusus saja yang akan menggunakan operator ini. 

Yang perlu diperhatikan bahwa, kedua operator ini digunakan untuk tipe data angka dalam bentuk bilangan biner.

### Operator Bitwise

Berikut adalah operator bitwise. Perlu diperhatikan, operand pada operator ini adalah tipe data integer.

| No   | Simbol | Contoh | Deskripsi                               |
| ---- | ------ | ------ | --------------------------------------- |
| 1    | &      | x & y  | Logika AND pada angka biner x dan y     |
| 2    | \|     | x\| y  | Logika OR pada angka biner x dan y      |
| 3    | ^      | x ^ y  | Logika XOR pada angka biner x dan y     |
| 4    | ~      | ~x     | Inversi bit 0 menjadi 1 atau sebaliknya |

### Operator Bit Shift

Berikut adalah operator bit shift.

| No   | Simbol | Contoh  | Deskripsi                                         |
| ---- | ------ | ------- | ------------------------------------------------- |
| 1    | \>>    | x >> 2  | Menggeser bit ke kanan sebanyak 2 kali            |
| 2    | <<     | x << 2  | Menggeser bit ke kiri sebanyak 2 kali             |
| 3    | \>>>   | x >>> 2 | Menggeser bit ke kanan sebanyak 2 kali (unsigned) |

### Latihan memahami operator bitwise

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut jika dijalankan. 

1. Kode program #1

   ```java
   public class OpBitwise {
       public static void main(String[] args) {
           int x = 0b0101;
           int y = 0b0011;
           int z = x & y;
           System.out.println(Integer.toBinaryString(x));
           System.out.println(Integer.toBinaryString(y));
           System.out.println(Integer.toBinaryString(z));
       }
   }
   ```
   
2. Kode program #2

   ```java
   public class OpBitwise {
       public static void main(String[] args) {
           int x = 0b0101;
           int y = 0b0011;
           int z = x | y;
           System.out.println(Integer.toBinaryString(x));
           System.out.println(Integer.toBinaryString(y));
           System.out.println(Integer.toBinaryString(z));
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class OpBitwise {
       public static void main(String[] args) {
           int x = 0b0101;
           int y = 0b0011;
           int z = ~x & y;
           System.out.println(Integer.toBinaryString(x));
           System.out.println(Integer.toBinaryString(y));
           System.out.println(Integer.toBinaryString(z));
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class OpBitwise {
       public static void main(String[] args) {
           int x = 0b0101;
           int y = 0b0011;
           int z = x | ~y;
           System.out.println(Integer.toBinaryString(x));
           System.out.println(Integer.toBinaryString(y));
           System.out.println(Integer.toBinaryString(z));
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class OpBitwise {
       public static void main(String[] args) {
           int x = 0b0101;
           int y = 0b0011;
           int z = x ^ ~y;
           System.out.println(Integer.toBinaryString(x));
           System.out.println(Integer.toBinaryString(y));
           System.out.println(Integer.toBinaryString(z));
       }
   }
   ```

   

### Latihan memahami operator bit shift

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut jika dijalankan. 

1. Kode program #1

   ```java
   public class OpBitshift {
       public static void main(String[] args) {
           int n = 0b1001;
           System.out.println(Integer.toBinaryString(n));
       }
   }
   ```

2. Kode program #2

   ```java
   public class OpBitshift {
       public static void main(String[] args) {
           byte n = 0b1001;
           System.out.println(Integer.toBinaryString( n ));
           System.out.println(Integer.toBinaryString( n << 1 ));
       }
   }
   ```

   

3. Kode program #3

   ```java
   public class OpBitshift {
       public static void main(String[] args) {
           byte n = 0b1001;
           System.out.println(Integer.toBinaryString( n ));
           System.out.println(Integer.toBinaryString( n >> 1 ));
       }
   }
   ```

   

4. Kode program #4

   ```java
   public class OpBitshift {
       public static void main(String[] args) {
           int n = 0xffff_fffe;
           System.out.println(Integer.toBinaryString( n ));
           System.out.println(Integer.toBinaryString( n >> 31 ));
       }
   }
   ```

   

5. Kode program #5

   ```java
   public class OpBitshift {
       public static void main(String[] args) {
           int n = 0xffff_fffe;
           System.out.println(Integer.toBinaryString( n ));
           System.out.println(Integer.toBinaryString( n >>> 31 ));
       }
   }
   ```

   

## Operator Object Comparison

Berikut adalah operator object comparison.

| No   | Keyword    | Contoh                    | Deskripsi                                                |
| ---- | ---------- | ------------------------- | -------------------------------------------------------- |
| 1    | instanceof | objectA instanceof ClassA | Menghasilkan true jika objectA adalah object dari ClassA |

Operator ini digunakan untuk menguji sebuah object adalah object dari sebuah class tertentu. Perhatikan kode berikut!

```java
public class OpInstance {
    public static void main(String[] args) {
        String nama = "Affandes";
        boolean cek = nama instanceof String;
        System.out.println(cek);
    }
}
```



## Operator Ternary

Berikut ini adalah operator ternary.

| No   | Simbol | Contoh                | Deskripsi                          |
| ---- | ------ | --------------------- | ---------------------------------- |
| 1    | ?:     | x == 2 ? true : false | Cara cepat untuk statement if-else |

Operator ini akan kita bahas lebih jauh pada bagian [Percabangan](Percabangan.md).

## Operator Precedence

Dalam satu instruksi bisa saja terdapat beberapa operator yang dioperasikan. Java dan beberapa bahasa pemrograman lainnya memiliki aturan tertentu tentang tingkatan prioritas operator apa saja yang harus dijalankan lebih dahulu, dan operator yang dijalankan kemudian. 

Aturan ini dinamakan **operator precedence**. Berikut adalah daftar urutannya.

| Operators            | Precedence                               |
| -------------------- | ---------------------------------------- |
| postfix              | `*expr*++ *expr*--`                      |
| unary                | `++*expr* --*expr* +*expr* -*expr* ~ !`  |
| multiplicative       | `* / %`                                  |
| additive             | `+ -`                                    |
| shift                | `<< >> >>>`                              |
| relational           | `< > <= >= instanceof`                   |
| equality             | `== !=`                                  |
| bitwise AND          | `&`                                      |
| bitwise exclusive OR | `^`                                      |
| bitwise inclusive OR | `|`                                      |
| logical AND          | `&&`                                     |
| logical OR           | `||`                                     |
| ternary              | `? :`                                    |
| assignment           | `= += -= *= /= %= &= ^= |= <<= >>= >>>=` |

Urutan di atas adalah urutan prioritas operator yang dijalankan. Semakin tinggi urutan operator semakin prioritas dijalankan terlebih dahulu. Perhatikan contoh kode program berikut ini!

```java
public class Operator {
    public static void main(String[] args) {

        int x = 10;
        int y = 11;

        boolean hasil = ++x + y++ < x-- + y--;
        System.out.println(hasil);

    }
}
```

Kode program di atas jika dijalankan akan menghasilkan output seperti berikut!

```shell
true
```



### Latihan memahami operator precedence

Perhatikan kode program berikut, jelaskan bagaimana kode program tersebut dijalankan!

1. Kode program #1

   ```java
   public class OpPrecedence {
       public static void main(String[] args) {
           int nilai = 2 + 2 * 2 - 2 % 2;
           System.out.println( nilai );
       }
   }
   ```

   

2. Kode program #2

   ```java
   public class OpPrecedence {
       public static void main(String[] args) {
           int x = 6;
           int y = 12;
           boolean hasil = x + x++ < y && y - x > 2;
           System.out.println( hasil );
       }
   }
   ```

   

## Tugas