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

