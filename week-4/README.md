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

### Responsive Web Design

Responsive Web Design adalah sebuah teknik yang digunakan untuk membuat sebuah website agar dapat menyesuaikan tampilan website sesuai dengan ukuran layar yang digunakan. Responsive Web Design dapat dilakukan dengan menggunakan CSS Media Query.

#### CSS Media Query

  CSS Media Query adalah sebuah aturan CSS yang digunakan untuk menentukan tampilan website sesuai dengan ukuran layar yang digunakan.

  ```css
  @media screen (max-width: 600px) {
    /* CSS disini akan dijalankan ketika ukuran layar maksimal 600px */
  }
  ```

  - `@media screen` : aturan CSS Media Query
  - `(max-width: 600px)` : aturan CSS Media Query yang digunakan untuk menentukan ukuran layar maksimal 600px

  ```css
  @media screen (min-width: 600px) {
    /* CSS disini akan dijalankan ketika ukuran layar minimal 600px */
  }
  ```

  - `@media screen` : aturan CSS Media Query
  - `(min-width: 600px)` : aturan CSS Media Query yang digunakan untuk menentukan ukuran layar minimal 600px

    ```css
    @media screen (min-width: 600px) and (max-width: 900px) {
      /* CSS disini akan dijalankan ketika ukuran layar minimal 600px dan maksimal 900px */
    }
    ```

    - `@media screen` : aturan CSS Media Query
    - `(min-width: 600px) and (max-width: 900px)` : aturan CSS Media Query yang digunakan untuk menentukan ukuran layar minimal 600px dan maksimal 900px

#### Macam-macam satuan relatif yang digunakan untuk responsive

  - #### `em`

    Satuan `em` adalah satuan yang digunakan untuk mengukur ukuran font. Satuan `em` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `rem`

    Satuan `rem` adalah satuan yang digunakan untuk mengukur ukuran font. Satuan `rem` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `vw`

    Satuan `vw` adalah satuan yang digunakan untuk mengukur ukuran layar. Satuan `vw` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `vh`

    Satuan `vh` adalah satuan yang digunakan untuk mengukur ukuran layar. Satuan `vh` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `vmin`

    Satuan `vmin` adalah satuan yang digunakan untuk mengukur ukuran layar. Satuan `vmin` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `vmax`

    Satuan `vmax` adalah satuan yang digunakan untuk mengukur ukuran layar. Satuan `vmax` merupakan satuan yang paling umum digunakan untuk responsive.

## Bootstrap 5

Bootstrap 5 adalah sebuah framework CSS yang digunakan untuk mempermudah dalam membuat tampilan website. Bootstrap 5 dapat digunakan untuk membuat tampilan website yang responsive.

  - #### Menggunakan CDN

    Menggunakan CDN adalah cara yang paling mudah untuk menggunakan Bootstrap 5. CDN adalah sebuah jaringan yang berfungsi untuk menyediakan file-file yang dibutuhkan oleh website.

    ```HTML
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0-alpha1/css/bootstrap.min.css"
      integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1"
      crossorigin="anonymous"
    />
    ```

  - #### Container

    Container adalah sebuah elemen yang berfungsi untuk mengatur tampilan website agar terlihat rapi.

    ```HTML
    <div class="container">
      <!-- Isi disini -->
    </div>
    ```

  - #### Row

    Row adalah sebuah elemen yang berfungsi untuk mengatur tampilan website agar terlihat rapi.

    ```HTML
    <div class="row">
      <!-- Isi disini -->
    </div>
    ```

  - #### Column

    Column adalah sebuah elemen yang berfungsi untuk mengatur tampilan website agar terlihat rapi.

    ```HTML
    <div class="col">
      <!-- Isi disini -->
    </div>
    ```

- ### Breakpoint

  - #### xs
    Breakpoint `xs` adalah breakpoint yang digunakan untuk ukuran layar minimal 0px.
  - #### sm
    Breakpoint `sm` adalah breakpoint yang digunakan untuk ukuran layar minimal 576px.
  - #### md
    Breakpoint `md` adalah breakpoint yang digunakan untuk ukuran layar minimal 768px.
  - #### lg
    Breakpoint `lg` adalah breakpoint yang digunakan untuk ukuran layar minimal 992px.
  - #### xl
    Breakpoint `xl` adalah breakpoint yang digunakan untuk ukuran layar minimal 1200px.
  - #### xxl
    Breakpoint `xxl` adalah breakpoint yang digunakan untuk ukuran layar minimal 1400px.

- ### Grid System
  - #### Grid System 1

    Grid System 1 adalah sebuah sistem yang digunakan untuk mengatur tampilan website agar terlihat rapi.

    ```HTML
    <div class="container">
      <div class="row">
        <div class="col">
          <!-- Isi disini -->
        </div>
        <div class="col">
          <!-- Isi disini -->
        </div>
        <div class="col">
          <!-- Isi disini -->
        </div>
      </div>
    </div>
    ```

  - #### Grid System 2

    Grid System 2 adalah sebuah sistem yang digunakan untuk mengatur tampilan website agar terlihat rapi.

    ```HTML
    <div class="container">
      <div class="row">
        <div class="col-4">
          <!-- Isi disini -->
        </div>
        <div class="col-4">
          <!-- Isi disini -->
        </div>
        <div class="col-4">
          <!-- Isi disini -->
        </div>
      </div>
    </div>
    ```

  - #### Grid System 3

    Grid System 3 adalah sebuah sistem yang digunakan untuk mengatur tampilan website agar terlihat rapi.

    ```HTML
    <div class="container">
      <div class="row">
        <div class="col-6">
          <!-- Isi disini -->
        </div>
        <div class="col-6">
          <!-- Isi disini -->
        </div>
      </div>
    </div>
    ```

  - #### Grid System 4

    Grid System 4 adalah sebuah sistem yang digunakan untuk mengatur tampilan website agar terlihat rapi.

    ```HTML
    <div class="container">
      <div class="row">
        <div class="col-8">
          <!-- Isi disini -->
        </div>
        <div class="col-4">
          <!-- Isi disini -->
        </div>
      </div>
    </div>
    ```
