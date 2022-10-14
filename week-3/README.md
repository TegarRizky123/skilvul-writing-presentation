## JavaScript Intermediate
### Array
- Array adalah struktur data yang digunakan untuk menyimpan sebuah kelompok data dalam satu tempat, array di javascript dapat menampung 
berbagai tipe data yang berbeda.
- Untuk membuat array kita perlu menggunakan square bracket atau kurung siku []
- Array pada javascript dihitung mulai dari index ke- 0 
- Contoh Array 
   - ```javascript 
     let Data = ['ini string', 20, true];
     // Index         0      , 1 , 2 
     console.log(Data);
     ```

- Untuk mengakses data array yang kita inginkan kita dapat menggunakan index value
   - ```javascript 
     let Data = ['ini string', 20, true];
     console.log(Data[1]);
     //output = 20
     ``` 

- Array Properti. Array memiliki 5 properti yang sering digunakan yaitu :
  - constructor
  - length
  - index 
  - input
  - prototype
  
- Length 
  yaitu mengembalikan nilai dari jumlah panjang data suatu array
  - Contoh length
  - ```javascript 
     let Data = ['ini string', 20, true];
     console.log(Data.length);
     ```
     
- Array Method atau biasa disebut dengan built in methods 
- Contoh array built in method :
- Untuk menambahkan item baru ke dalam array kita bisa menggunakan push() dan unshift()
   - Push () untuk menambahkan item di index terakhir
   ```javascript 
     let buah = ['anggur', 'rambutan', 'pepaya'];
     console.log(buah); 
     //output ['anggur', 'rambutan', 'pepaya']
     
     buah.push('jambu');
     console.log(buah);
     //output ['anggur', 'rambutan', 'pepaya', 'jambu']
     ```
     
   - Unshift () untuk menambahkan item di index awal
   ```javascript 
     let buah = ['anggur', 'rambutan', 'pepaya'];
     console.log(buah); 
     //output ['anggur', 'rambutan', 'pepaya']
     
     buah.unshift('jambu');
     console.log(buah);
     //output ['jambu', 'anggur', 'rambutan', 'pepaya']
     ```
   
- Untuk menghapus item array kita bisa menggunakan pop() dan shift()
   - Pop () untuk menghapus item di index terakhir
   ```javascript 
     let buah = ['anggur', 'rambutan', 'pepaya'];
     console.log(buah); 
     //output ['anggur', 'rambutan', 'pepaya']
     
     buah.pop();
     console.log(buah);
     //output ['anggur', 'rambutan']
     ```
     
   - Shift () untuk menghapus item di index awal 
      ```javascript 
     let buah = ['anggur', 'rambutan', 'pepaya'];
     console.log(buah); 
     //output ['anggur', 'rambutan', 'pepaya']
     
     buah.shift();
     console.log(buah);
     //output ['rambutan', 'pepaya']
     ```
   
- Untuk mengurutkan array kita bisa menggunakan sort ()
  ```javascript 
     let angka = [1,3,5,2,4];
     console.log(angka);
     //output [1,3,5,2,4]
     
     angka.sort()
     console.log(angka);
     //output [1,2,3,4,5]
  ```

- Looping pada Array Built in methods untuk melakukan looping pada array ada .map() dan .forEach()
- Contoh looping pada array
  - .forEach() digunakan untuk melakukan iterasi dalam mengakses elemen array 
  ```javascript
  let colors = ['blue', 'red', 'yellow', 'green'];
  colors.forEach(data => {
  console.log(data)
  ```
  
  - .map() digunakan untuk melakukan perulangan sambil mengecek/melakukan operasi terhadap setiap elemen array, 
  lalu memberikan nilai balik berupa array baru tanpa mengubah nilai pada array yang lama.
  ```javascript
  let arrBuah = ["jeruk", "semangka", "pepaya", "rambutan"]
  let buahSegar = arrBuah.map((item) => {
    return item + " " + "segar"
  })
  console.log(buahSegar)
  //output ['jeruk segar', 'semangka segar', 'pepaya segar', 'rambutan segar']  
  ```
  
### Multidimensional Array
- Multidimensional array bisa dianalogikan sebagai array of array
- Multidimensional array sama seperti matriks yaitu memiliki 2 dimensi (x,y)
    ```javascript
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    console.log(inventory);
    ```
- Mengakses multidimensional array
     ```javascript
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    console.log(inventory[1][0]);
    ```
- Penggunaan built in method pada multidimensional array
    ```javascript
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    inventory.push(['Hoodie', 2]);
    console.log(inventory);
    ```

### Object
- Di JavaScript, objek bisa digambarkan sebagai sesuatu yang memiliki properti dan nilai.
- Membuat object
```javascript
  let namaObjek = {
  namaProperti1: nilai1,
  namaProperti2: nilai2
  };
```

- Mengakses properti ada 2 cara yaitu :
- Dot Notation 
  ```javascript
  let mahasiswa = {
  nama: 'tegar',
  umur: 19,
  hobi: 'game'
  };
  
  console.log(mahasiswa.nama);
  // output 'tegar'
  ```
  
- Bracket Notation
```javascript
  let mahasiswa = {
  nama: 'tegar',
  umur: 19,
  hobi: 'game'
  };
  
  console.log(orang["nama"]);
  // output 'tegar'
```

- Mengupdate value properti pada sebuah object 
```javascript
   let hewan = {
   nama: "kucing",
   kaki: 4,
   warna: "putih",
   };
  
  console.log(hewan.warna);
  // output "putih"
  
  //merubah value dari properti warna
  hewan.warna = "hitam";
  console.log(hewan.warna);
  // output "hitam"
```

- Menghapus properti pada sebuah object
```javascript
    let hewan = {
    nama: "kucing",
    kaki: 4,
    warna: "putih",
    };
    
    console.log(hewan);
    //output {nama: "kucing", kaki: 4, warna:"putih"}
    delete hewan.warna
    console.log(hewan);
    //output {nama: "kucing", kaki:"4"}
```

- Method object
```javascript

const greeting = {
  welcome: function () {
    return "halo selamat datang";
  },
  afterPay: function () {
    return "Terimakasih sudah membeli produk kami";
  },
};

console.log(greeting.welcome());
console.log(greeting.afterPay());

let siswa = {
  nama: "dila",
  umur: 17,
  hobi: "membaca",
};

console.log(siswa);
// [nama, umur, hobi]

console.log(Object.keys(siswa));
console.log(Object.values(siswa));
```

- Nested object
  object yang berasal dari turunan object lainnya
```javascript
                       
let buku = {
  judul: "tips jago javascript",
  tahun: 2022,
  penulis: {
    penulis1: {
      nama: "Reyhan",
      umur: 28,
      kota: "jakarta",
    },
    penulis2: {
      nama: "aby",
      umur: 25,
      kota: "bandung",
    },
  },
};

console.log(buku);
console.log(buku.penulis.penulis1.nama);
console.log(buku.penulis.penulis2.umur);
```
- Looping pada object
    Ada 4 cara looping pada object.
   - for in
      ```javascript
      let motor = {
        tipe: "Kawasaki",
        model: "350",
        warna: "white",
      };
      for (let i in motor) {
        console.log(i);
      }
      ```
   - for of
      ```javascript
      let motor = {
        tipe: "Kawasaki",
        model: "3500",
        warna: "white",
      };
      for (let i of Object.keys(motor)) {
        console.log(i);
      }
      ```
   - forEach
      ```javascript
      let motor = {
        tipe: "Kawasaki",
        model: "350",
        warna: "white",
      };
      Object.keys(motor).forEach((i) => {
        console.log(i);
      });
      ```
   - map
      ```javascript
      let motor = {
        tipe: "Kawasaki",
        model: "350",
        warna: "white",
      };
      let motor2 = Object.keys(motor).map((i) => {
        return i;
      });
      console.log(motor2);
      ```
      
### Modules & Recursive
- Modules memungkinkan untuk memecah kode menjadi file terpisah sehingga mempermudah untuk maintain code
- JavaScript Module bergantung pada pernyataan impor dan ekspor
- Recursive adalah fungsi yang memanggil dirinya sendiri sampai suatu kondisi tertentu terpenuhi
- A new paradigm :
  - Procedural
  - Conditional
  - Looping
  - Modular (function)
  - Recursive
- Ciri dari recursive:
  - Fungsi recursive memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. 
  - fungsi recursive selalu memaanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya.
- Contoh mencari nilai pangkat 
```javascript
    function faktorial(n) {
  if (n == 1) {
    return 1;
  } else {
    return n * faktorial(n - 1);
  }
}

console.log(faktorial(4))
// output = 24
```

###  Asynchronous 
- Asynchronous sebuah teknik yang menyelesaikan fungsi secara paralel
- Penggunaan asynchronous dapat dilakukan jika kita ingin mengambil data dari database
- Mengapa perlu menggunakan asynchronous? Asynchronous dibutuhkan ketika ada proses yangg membutuhkan waktu lama. Jadi kita bisa mengerjakan proses yg lain secara paralel.
- Callbacks adalah suatu function namun cara pengeksekusiannya yang berbeda yaitu hanya mengeksekusi pada point tertentu.
- Ada dua function yang digunakan untuk mengatur penjadwalan asynchronous adalah **setTimeout** function dan **setInterval** function 
- contoh penggunaan function
  - setTimeout
```javascript
setTimeout(() => {
  console.log("Cuci baju"); 
}, 1000);
console.log("Menyapu");
console.log("Mengepel");
console.log("Memasak");

// 1000 ms = 1 second
// Output:
// Menyapu
// Mengepel
// Memasak
// Cuci baju
```
   
  - setInterval
```javascript
setInterval(() => {
  console.log("Cuci baju"); 
}, 3000);
console.log("Menyapu");
console.log("Mengepel");
console.log("Memasak");

// 3000 ms = 3 second
// Output:
// Menyapu
// Mengepel
// Memasak
// Cuci baju (x time)
// Cuci baju akan dijalankan setiap 3 detik sekali
```

- Contoh Penggunaan Callback pada Asynchronous
  ```javascript
    function p1() {
    console.log('p1 done')
  }

    function p2(callback) {
    setTimeout(
    function() {
    console.log('p2 done')
      callback()
    },100
    )
  }

  function p3() {
  console.log('p3 done')
  }
  p1()
  p2(p3)
  ```
  
- Asynchronous - Promise merupakan suatu object dan digunakan hanya untuk satu event dengan menyimpan hasil dari sebuah operasi asynchronous baik itu hasil yang diinginkan (resolved value) atau alasan kenapa operasi itu gagal (failure reason)
  ```javascript
    function GetUser(id) {
    return new Promise((resolve, reject) => {
    if (id !== "" && id !== undefined) {
      reesolve (id);
    } else {
      reject ("ID Harus di Isi");
        }
    });
    }
    
    GetUser( ) 
    .then((response) => {
    console.log(response);
     })
     .catch((error) => {
    console.log(error);
    });
  ```
- Asynchronous - Async-Await merupakan fitur yang hadir sejak ES2017 bekerja dengan cara menunda eksekusi hingga proses asynchronous selesai
- Asynchronous - Fetch merupakan cara baru dalam melakukan network request yang memanfaatkan sebuah Promise dalam penggunaanya. Karen Fetch mengembalikan sebuah Promise maka respon handling yang digunakan adalah **then** jika promise mengembalikan resolve dan **catch** jika promise mengembalikan nilai reject
  ```javascript
    fetch("https://pokeapi.co/api/v2/pokemon/pikachu/", {
    method: "GET"
    })
     .then((response) => {
      return response.json();
    })
    .then((data) => {
     console.log(data);
     })
    .catch((error) => {
    console.log(error);
    });
  ```
  
### Web Storage
- Web Storage adalah wadah untuk sebuah data yang digunakan untuk penyimpanan data yang terikat di browsernya
- Jenis Web Storage yang umum digunakan yaitu :
  - Local Storage
  - Session storage
  - Cookies

- Local Storage adalah wadah untuk menampung data user yang digunakan di penyimpanan lokal dan tidak akan hilang selama user tidak menghapus data local storage pada web browser

- Session Storage adalah adalah wadah untuk menampung data user pada sebuah session dan perlu diingat jika kita membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window. dan Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.

- Cookies adalah sebuah cara untuk menyimpan data di browser. Cookie akan menyimpan data di browser dan data tersebut akan tetap ada meskipun browser ditutup.
