## JavaScript 
### **Array**
- **Array** adalah struktur data yang digunakan untuk menyimpan sebuah kelompok data dalam satu tempat, array di javascript dapat menampung 
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

- **Array Properti**. Array memiliki 5 properti yang sering digunakan yaitu :
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
     
- **Array Method**  atau biasa disebut dengan built in methods 
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

- **Looping pada Array**. Built in methods untuk melakukan looping pada array ada .map() dan .forEach()
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
  
### **Multidimensional Array**
   > Multidimensional array bisa dianalogikan sebagai array of array
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
    
