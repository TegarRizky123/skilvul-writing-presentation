# Writing And Presentation week 2

## **JavaScript Dasar**
- ### Looping
  Looping merupakan statement yang mengulang suatu instruksi hingga kondisi terpenuhi atau jika kondisi stop atau berhenti

  - Ada 3 macam looping
   - for loop
   - while loop
   - nested loop

- For loop
   Jika kita ingin menggunakan for loop pastikan kita tau nilai seberapa banyak nilai pasti untuk penggulangannya
```
  let nilai = 1 ; 
  for (nilai; nilai <= 20 ; nilai++){
    console.log(nilai) 
  } 
```

- While loop
  While loop akan menjalankan intruksi pengulangan kondisi bernilai true, gunakan while loop jika kita tidak mengetahui jumlah pasti pengulangan.

```
   let hitung = 1;
  
   while (hitung < 10) {
    console.log("Hitung");
    hitung++;
   }
```

- Do while
```
  do {
    console.log("Hitung");
    hitung++;
  } while (hitung <= 10);
```

- Nested loop 
  Nested loop adalah dimana kita membuat perulangan didalam perulangan
 
- ### Scope
  Scope adalah konsep dalam flow data variabel,menentukan sebuah variabel bisa diakses pada scope tertentu atau tidak.

- Global Scope
  Global Scope berarti variabel yang kita buat bisa diakses dimanapun dalam suatu file,Agar menjadi global scope suatu variabel harus dideklarasikan diluar {}

```
   let nama = "Tegar";
   function greeting(){
     return nama;
   }
   console.log(nama);
```

- Local Scope
  Local Scope kebalikan dari Global Scope yang dimana kita tidak dapat mengakses variabel dimanapun dalam suatu file kecuali jika kita mengaksesnya didalam sebuah 
  blocks,sebuah variabel akan menjadi local scope jika variabel tersebut dideklarasikan di dalam {}

```
   function greetings() {
    let nama = "Tegar";
    return nama;
   }
    console.log(greetings());
    console.log(nama);
```  

- ### Function
  Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task atau 1 fitur,yang dimana jika kita membutuhkannya kita bisa menggunakannya lagi

- Membuat Function
  - ``function`` merupakan function keyword
  - ``greetings`` merupakan sebuah nama function atau identifier
  - didalam ``{}`` merupakan function body
```
   function greetings() {
    return "Hello world!";
   }
```

- Memanggil Function
```
   greetings();
   console.log(greetings());
```

- Parameter
  Parameter adalah syarat input yang harus dimasukkan ke dalam suatu fungsi dan dideklarasikan bersama dengan deklarasi fungsi. pada contoh dibawah ini number1 dan       number 2 adalah parameter.

- Argument
  Argument adalah nilai yang dimasukkan ke dalam suatu fungsi,sesuai dengan persyaratan parameter dimana argument dituliskan bersamaan dengan pemanggilan fungsi. pada contoh dibawah ini 3 dan 4 adalah argument.

```
   function operasiPenjumlahan(number1, number2){
   return number1 + number2;
   }
   
   console.log(operasiPenjumlahan(3, 4))
```

- Arrow Function 
  Adalah cara lain menuliskan function, ini adalah fitur terbaru yang ada pada ES6 (JavaScript Version)
  
```
   const greetings = () => {
    return `Hello world!`;
   };
   console.log(greetings());
```

- ### DataType Prototype & Method

- Protoype
  Prototype adalah sebuah object yang berisi method-method yang dapat digunakan oleh object lain. Prototype dapat diakses dengan menggunakan tanda titik (.) setelah     nama object.Pada contoh di bawah ini, method toLowerCase() merupakan method yang ada di dalam prototype String. Method toLowerCase() akan mengubah string menjadi huruf kecil.
```
   let nama = "TEGAR";
   console.log(nama.toLowerCase());
```

- Method
  Method adalah sebuah function yang berada dalam type data,method digunakan untuk merubah value dari suatu object seperti contoh diatas.method toLowerCase() merupakan 
  method yang ada dalam type data string yang akan mengubah huruf kapital menjadi huruf kecil.
  
- String Prototype
  untuk mengetahui jumlah karakter dalam sebuah string mengguunakan length
```
   let nama = "Tegar Risqy Yulian Santoso;
   console.log(nama.length); // 26
```

- Method String
  - Untuk mengubah karakter string menjadi huruf kecil 
  ```
  console.log(nama.toLowerCase()); //tegar risqy yulian santoso
  ```
  
  - Untuk mengubah karakter string menjadi huruf besar
  ```
  console.log(nama.toUpperCase()); //TEGAR RISQY YULIAN SANTOSO
  ```

  - Untuk mengembalikan karakter berdasarkan posisi dari indeks nya contoh kita ingin mengambil huruf t nya maka kita tisi indeks ke 0
  ```
  console.log(nama.charAt(0)); // t
  ```
  
  - Untuk mencari karakter dan jika ditemukan akan mengembalikan nilai true dan jika ditemukan akan mengembalikan false
  ```
  console.log(nama.includes("santoso")); // true
  ```
  
  - Untuk membagi dari string yang akan kita tuju kemudian dipisah berdasarkan spasi menjadi sebuah data array
  ```
  console.log(nama.split(" ")); // ['tegar', 'risqy', 'yulian', 'santoso']
  ```

- Method Number
  - Untuk mengubah number menjadi sebuah string
  ```
  let angka = 20;
  angka.toString(); // '20'
  ```
  
  - Untuk mengetahui karakter number atau bukan kita bisa menggunakan isNAN, jika karakter string maka akan mengembalikan nilai true, dan jika karakter number akan         mengembalikan nilai false
  ```
  console.log(isNaN(1)); // false
  console.log(isNaN("tegar")); // true
  ```
  
  - Untuk menentukan jumlah angka yang akan kita ambil dibelakang koma dan mengembalikan nilai dalam bentuk string
  ```
  let pi = 3.14123212
  pi.toFixed(2); // '3.14'
  ```
  
- Method Math
  - Untuk mengubah angka - menjadi +
  ```
  console.log(Math.abs(-1)); // 1
  ```
  
  - Untuk menghitung hasil dari pangkat
  ```
  let bilangan = 6;
  let pangkat = 2;
  console.log(Math.pow(bilangan, pangkat)); // 36
  ```
  
  - Untuk menghitung akar kuadrat
  ```
  console.log(Math.sqrt(bilangan)); // 2.4494897427
  ```
  
  - Untuk mengitung ankar pangkat 3
  ```
  console.log(Math.cbrt(bilangan)); // 1.8171205928
  ```
  
  - Untuk membulatkan angka desimal menjadi bilangan bulat
  ```
  let bilangan1 = 7.7;
  console.log(Math.round(bilangan1)); // 8
  ```
  
  - Untuk membulatkan angka desimal menjadi bilangan bulat ke bawah
  ```
  console.log(Math.floor(bilangan1)); // 7
  ```
  
  - Untuk membulatkan angka desimal menjadi bilangan bulat ke atas
  ```
  console.log(Math.ceil(bilangan1)); // 8
  ```
  
  - Untuk mencari angka random
  ```
  console.log(Math.random());
  ```
  
  - Untuk mencari angka terbesar di antara parameter
  ```
  console.log(Math.max(1, 4, 6, 7, 10)); // 10
  ```
  
  - Untuk mencari angka terkecil diantara parameter
  ```
  console.log(Math.min(1, 4, 6, 7, 10)); // 1
  ```
    
