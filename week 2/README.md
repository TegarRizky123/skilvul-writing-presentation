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
```javascript
  let nilai = 1 ; 
  for (nilai; nilai <= 20 ; nilai++){
    console.log(nilai) 
  } 
```

- While loop
  While loop akan menjalankan intruksi pengulangan kondisi bernilai true, gunakan while loop jika kita tidak mengetahui jumlah pasti pengulangan.

```javascript
   let hitung = 1;
  
   while (hitung < 10) {
    console.log("Hitung");
    hitung++;
   }
```

- Do while
```javascript
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

```javascript
   let nama = "Tegar";
   function greeting(){
     return nama;
   }
   console.log(nama);
```

- Local Scope
  Local Scope kebalikan dari Global Scope yang dimana kita tidak dapat mengakses variabel dimanapun dalam suatu file kecuali jika kita mengaksesnya didalam sebuah 
  blocks,sebuah variabel akan menjadi local scope jika variabel tersebut dideklarasikan di dalam {}

```javascript
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
```javascript
   function greetings() {
    return "Hello world!";
   }
```

- Memanggil Function
```javascript
   greetings();
   console.log(greetings());
```

- Parameter
  Parameter adalah syarat input yang harus dimasukkan ke dalam suatu fungsi dan dideklarasikan bersama dengan deklarasi fungsi. pada contoh dibawah ini number1 dan       number 2 adalah parameter.

- Argument
  Argument adalah nilai yang dimasukkan ke dalam suatu fungsi,sesuai dengan persyaratan parameter dimana argument dituliskan bersamaan dengan pemanggilan fungsi. pada contoh dibawah ini 3 dan 4 adalah argument.

```javascript
   function operasiPenjumlahan(number1, number2){
   return number1 + number2;
   }
   
   console.log(operasiPenjumlahan(3, 4))
```

- Arrow Function 
  Adalah cara lain menuliskan function, ini adalah fitur terbaru yang ada pada ES6 (JavaScript Version)
  
```javascript
   const greetings = () => {
    return `Hello world!`;
   };
   console.log(greetings());
```

- ### DataType Prototype & Method

- Protoype
  Prototype adalah sebuah object yang berisi method-method yang dapat digunakan oleh object lain. Prototype dapat diakses dengan menggunakan tanda titik (.) setelah     nama object.Pada contoh di bawah ini, method toLowerCase() merupakan method yang ada di dalam prototype String. Method toLowerCase() akan mengubah string menjadi huruf kecil.
```javascript
   let nama = "TEGAR";
   console.log(nama.toLowerCase());
```

- Method
  Method adalah sebuah function yang berada dalam type data,method digunakan untuk merubah value dari suatu object seperti contoh diatas.method toLowerCase() merupakan 
  method yang ada dalam type data string yang akan mengubah huruf kapital menjadi huruf kecil.
  
- String Prototype
  untuk mengetahui jumlah karakter dalam sebuah string mengguunakan length
```javascript
   let nama = "Tegar Risqy Yulian Santoso;
   console.log(nama.length); // 26
```

- Method String
  - Untuk mengubah karakter string menjadi huruf kecil 
  ```javascript
  console.log(nama.toLowerCase()); //tegar risqy yulian santoso
  ```
  
  - Untuk mengubah karakter string menjadi huruf besar
  ```javascript
  console.log(nama.toUpperCase()); //TEGAR RISQY YULIAN SANTOSO
  ```

  - Untuk mengembalikan karakter berdasarkan posisi dari indeks nya contoh kita ingin mengambil huruf t nya maka kita tisi indeks ke 0
  ```javascript
  console.log(nama.charAt(0)); // t
  ```
  
  - Untuk mencari karakter dan jika ditemukan akan mengembalikan nilai true dan jika ditemukan akan mengembalikan false
  ```javascript
  console.log(nama.includes("santoso")); // true
  ```
  
  - Untuk membagi dari string yang akan kita tuju kemudian dipisah berdasarkan spasi menjadi sebuah data array
  ```javascript
  console.log(nama.split(" ")); // ['tegar', 'risqy', 'yulian', 'santoso']
  ```

- Method Number
  - Untuk mengubah number menjadi sebuah string
  ```javascript
  let angka = 20;
  angka.toString(); // '20'
  ```
  
  - Untuk mengetahui karakter number atau bukan kita bisa menggunakan isNAN, jika karakter string maka akan mengembalikan nilai true, dan jika karakter number akan         mengembalikan nilai false
  ```javascript
  console.log(isNaN(1)); // false
  console.log(isNaN("tegar")); // true
  ```
  
  - Untuk menentukan jumlah angka yang akan kita ambil dibelakang koma dan mengembalikan nilai dalam bentuk string
  ```javascript
  let pi = 3.14123212
  pi.toFixed(2); // '3.14'
  ```
  
- Method Math
  - Untuk mengubah angka - menjadi +
  ```javascript
  console.log(Math.abs(-1)); // 1
  ```
  
  - Untuk menghitung hasil dari pangkat
  ```javascript
  let bilangan = 6;
  let pangkat = 2;
  console.log(Math.pow(bilangan, pangkat)); // 36
  ```
  
  - Untuk menghitung akar kuadrat
  ```javascript
  console.log(Math.sqrt(bilangan)); // 2.4494897427
  ```
  
  - Untuk mengitung ankar pangkat 3
  ```javascript
  console.log(Math.cbrt(bilangan)); // 1.8171205928
  ```
  
  - Untuk membulatkan angka desimal menjadi bilangan bulat
  ```javascript
  let bilangan1 = 7.7;
  console.log(Math.round(bilangan1)); // 8
  ```
  
  - Untuk membulatkan angka desimal menjadi bilangan bulat ke bawah
  ```javascript
  console.log(Math.floor(bilangan1)); // 7
  ```
  
  - Untuk membulatkan angka desimal menjadi bilangan bulat ke atas
  ```javascript
  console.log(Math.ceil(bilangan1)); // 8
  ```
  
  - Untuk mencari angka random
  ```javascript
  console.log(Math.random());
  ```
  
  - Untuk mencari angka terbesar di antara parameter
  ```javascript
  console.log(Math.max(1, 4, 6, 7, 10)); // 10
  ```
  
  - Untuk mencari angka terkecil diantara parameter
  ```javascript
  console.log(Math.min(1, 4, 6, 7, 10)); // 1
  ```
- ### Primitive & Non Primitive

- Primitive 
  - String
  - Number
  - Boolean
  - Null
  - Undefined
- Non Primitive
  - Object
  - Function
  - Array
  - Date
  - RegExp
  - Error

## DOM

- ### Apa itu Document Object Model (DOM)?

  Document Object Model (DOM) adalah sebuah interface yang memungkinkan kita untuk mengakses dan memanipulasi elemen HTML dan CSS. DOM menyediakan sebuah API yang memungkinkan kita untuk mengubah struktur halaman web, style, dan konten. DOM juga menyediakan sebuah API untuk membuat aplikasi yang interaktif dan menarik.

- ### Apa itu DOM Tree?

  DOM Tree adalah sebuah struktur data yang merepresentasikan struktur halaman web. DOM Tree terdiri dari node-node yang saling berhubungan. Setiap node memiliki tipe yang berbeda. Nodetipe element disebut element node. Node tipe text disebut text node. Node tipe comment disebut comment node. Node tipe document disebut document node. Node tipe attribute disebut attribute node.

- ### Apa itu DOM Node?

  DOM Node adalah sebuah objek yang merepresentasikan sebuah elemen HTML atau CSS. DOM Node memiliki properti dan metode yang dapat digunakan untuk mengakses dan memanipulasi elemen HTML atau CSS. DOM Node memiliki tipe yang berbeda. Tipe dari DOM Node dapat dilihat pada gambar di bawah ini.

- ### Apa manfaat DOM?
  - Memanipulasi elemen HTML dan CSS
  - Mengubah struktur halaman web
  - Mengubah style halaman web
  - Mengubah konten halaman web
  - Membuat aplikasi yang interaktif dan menarik

## Javascript Dasar - DOM - Selecting Element

- ### Cara mengakses DOM Node

  - Menggunakan ID
    ```javascript
    const title = document.getElementById("title");
    ```
  - Menggunakan Class
    ```javascript
    const title = document.getElementsByClassName("title");
    ```
  - Menggunakan Tag Name
    ```javascript
    const title = document.getElementsByTagName("h1");
    ```
  - Menggunakan Query Selector
    ```javascript
    const title = document.querySelector("#title");
    const title = document.querySelector(".title");
    const title = document.querySelector("h1");
    ```

- ### Cara mengakses DOM Node - Child

  - Menggunakan Child Nodes
    ```javascript
    const name = document.getElementById("name");
    const childNodes = name.childNodes;
    ```
  - Menggunakan Children
    ```javascript
    const name = document.getElementById("name");
    const children = name.children;
    ```
  - Menggunakan First Child
    ```javascript
    const name = document.getElementById("name");
    const firstChild = name.firstChild;
    ```
  - Menggunakan First Element Child
    ```javascript
    const name = document.getElementById("name");
    const firstElementChild = name.firstElementChild;
    ```
  - Menggunakan Last Child
    ```javascript
    const name = document.getElementById("name");
    const lastChild = name.lastChild;
    ```
  - Menggunakan Last Element Child
    ```javascript
    const name = document.getElementById("name");
    const lastElementChild = name.lastElementChild;
    ```

- ### Cara mengakses DOM Node - Parent

  - Menggunakan Parent Node
    ```javascript
    const name = document.getElementById("name");
    const parentNode = name.parentNode;
    ```
  - Menggunakan Parent Element
    ```javascript
    const name = document.getElementById("name");
    const parentElement = name.parentElement;
    ```

## Javascript Dasar - DOM - Manipulating Elements

- ### Cara mengubah DOM Node

  - Menggunakan Inner HTML
    ```javascript
    const title = document.getElementById("title");
    title.innerHTML = "Hello World";
    ```
  - Menggunakan Inner Text
    ```javascript
    const title = document.getElementById("title");
    title.innerText = "Hello World";
    ```
  - Menggunakan Text Content
    ```javascript
    const title = document.getElementById("title");
    title.textContent = "Hello World";
    ```
  - Menggunakan Class List
    ```javascript
    const title = document.getElementById("title");
    title.classList.add("red");
    title.classList.remove("red");
    title.classList.toggle("red");
    ```
  - Menggunakan Attributes
    ```javascript
    const title = document.getElementById("title");
    title.setAttribute("id", "title");
    title.removeAttribute("id");
    ```

## Javascript Dasar - DOM - Manipulating Styles

- ### Cara mengubah style DOM Node

  - Menggunakan Style
    ```javascript
    const title = document.getElementById("title");
    title.style.color = "red";
    title.style.backgroundColor = "black";
    title.style.fontSize = "50px";
    ```
  - Menggunakan CSS Text
    ```javascript
    const title = document.getElementById("title");
    title.style.cssText =
      "color: red; background-color: black; font-size: 50px;";
    ```
    
## Javascript Dasar - DOM - Events

- ### Cara menambahkan event pada DOM Node

  - Menggunakan Event Listener
    ```javascript
    const title = document.getElementById("title");
    title.addEventListener("click", function () {
      console.log("Hello World");
    });
    ```
  - Menggunakan Event Handler
    ```javascript
    const title = document.getElementById("title");
    title.onclick = function () {
      console.log("Hello World");
    };
    ```

## Javascript Dasar - DOM - Forms

- ### Cara mengakses DOM Node - Form

  - Menggunakan Form
    ```javascript
    const form = document.getElementById("form");
    ```
  - Menggunakan Form - Input
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    ```
  - Menggunakan Form - Input - Value
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    const value = input.value;
    ```
  - Menggunakan Form - Input - Type
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    const type = input.type;
    ```
  - Menggunakan Form - Input - Placeholder
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    const placeholder = input.placeholder;
    ```
  - Menggunakan Form - Input - Checked
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    const checked = input.checked;
    ```
  - Menggunakan Form - Input - Disabled
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    const disabled = input.disabled;
    ```
  - Menggunakan Form - Input - Required
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    const required = input.required;
    ```
  - Menggunakan Form - Input - Max Length
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    const maxLength = input.maxLength;
    ```
  - Menggunakan Form - Input - Min Length
    ```javascript
    const form = document.getElementById("form");
    const input = form.input;
    const minLength = input.minLength;
    ```
 
