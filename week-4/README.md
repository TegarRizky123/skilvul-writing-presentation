## JavaScript Intermediate

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
  ```javascript
  let nonton = (kondisi) => {
    return new Promise((resolve, reject) => {
      if (kondisi == "jalan") {
        resolve("nonton terpenuhi")
      }
      reject("batal nonton")
    })
  }
  async function asyncNonton() {
    try {
      let result = await nonton("jalan")
      console.log(result); // output = nonton terpenuhi
    } catch (error) {
      console.log(error)
    }
  }
  asyncNonton()  
  ```
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
 
### Git dan Github lanjutan
- git log : untuk melihat history perubahan yang telah dilakukan pada suatu project
- git checkout : untuk berpindah branch atau membuat branch baru
- git reset    : untuk merubah ke commit sebelumnya
- git Revert : untuk membatalkan perubahan yang terjadi di git tanpa menghapus git commit sebelumnya
- Clone yaitu menggandakan atau mengcopy sebuah project
- Fork yaitu sama halnya dengan clone namun langsung mengambil file dari repository

