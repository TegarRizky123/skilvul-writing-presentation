# Writing and Presentation Test Week 1

## Materi 1 minggu 

- [Unix Command Line](#unix-command-line)
- [Git dan Github](#git-dan-github)
- [HTML](#html)
- [CSS](#css)
- [Algoritma dan struktur data](#algoritma-dan-struktur-data)
- [Javascript Dasar](#javascript-dasar)

## Unix Command Line 
- Shell merupakan sebuah program yang digunakan oleh user supaya dapat berinteraksi dengan sistem operasi
- Contoh terminal basic atau basic shell yang sudah terinstall secara default di windows adalah powershell dan commandprompt (CMD)
- Shell berbasis teks disebut command line interface (CLI) misalnya : Sh,bash,zsh dan cmd
- Selain CLI kita juga punya shell berbasis graphical user interface (GUI) misalnya : windows,macOS atau ubuntu
- Untuk mengakses CLI kita menggunakan sebuah terminal emulator
- Command Line interface merupakan tampilan dari sebuah terminal yang digunakan untuk kita menaruh command untuk menjalankan suatu program, mengelola file, dan berinteraksi dengan komputer.
 (picture terminal git)
- ### File system structure
- Sistem operasi menggunakan sesuatu yang disebut file system
- Sebuah file system mengatur bagaimana sebuah data disimpan didalam sebuah system
- Dalan sistem operasi windows menyusun file nya dan directory nya menggunakan struktur yang bentuknya mirip dengan pohon
- (gambar struktur direktori)
- ### Command
- pwd digunakan untuk melihat posisi directory yang sedang aktif/posisi sekarang user berada
- ls digunakan untuk melihat isi files suatu directory 
- kemudian jika kita ingin melihat sebuah directory yang di sembunyikan bisa menggunakan perintah ls -a 
- cd merupakan command untuk berpindah dari satu directory ke directory lain
- mkdir digunakan untuk membuat directory baru
- Touch digunakan untuk membuat file
- mkdir merupakan command untuk membuat directory baru  
- cp digunakan untuk menyalin file 
- kemudian jika kita ingin menyalin sebuah directory kita bisa menggunakan perintah cp -r
- mv digunakan untuk memindahkan sebuah file maupun directory 
- mv juga dapat digunakan untuk mengganti nama file maupun directory
- rm merupakan command untuk menghapus sebuah file 
- kemudian jika ingin menghapus sebuah directory kita bisa menggunakan perintah rm -r

## Git dan Github
- ### Git
     Sebuah sistem yang merekam perubahan repository yang ada diproject dari waktu ke waktu
- ### Github
    Salah satu penyedia jasa hosting git repository yang populer selain Gitlab dan Bitbucket 
- ### Kenapa Git & Github wajib digunakan oleh developer ?
     Alasan  kenapa Git & Github wajib bagi seorang developer singkat saja karena untuk saling berkolaborasi dengan para developer lain dalam mengembangkan suatu aplikasi

- ### Perbedaan Git dan Github
| <div align="center">Git       </div>               |<div align="center"> Github  </div>   |
| :------ |   ------:       |
| Meng-install software di penyimpanan lokal|Host melalui layanan cloud|
| Akses secara offline|Akses secara online|
| Open sourced licensed|Pilihan bagi pengguna gratis dan pengguna berbayar|

- ### Command
- `git init` digunakan untuk membuat repository baru
- `git config global user.name` dan `git config global global user.email` untuk mengkonfigurasi git
- `git config --list` untuk mengecek hasil konfigurasi
- `git add` untuk menambahkan file baru
- `git commit` untuk menyimpan perubahan ke database, kemudian jika ingin menambahkan pesan apa saja yang baru disimpan bisa gunakan -m 
- `git remote` untuk menghubungkan repository github dan lokal yang sudah kita buat
- `git push` untuk mengirim perubahan ke server
- `git clone` untuk melakukan cloning dari server github ke lokal

## HTML

- ### Peranan HTML 
  Peranan Hypertext Markup Language atau biasa disebut HTML adalah sebuah kerangka awal (struktur) yang harus dibuat terlebih dahulu dalam pembuatan website

- ### Tools HTML
- Code editor : Visual Studio Code,Sublime,Notepad++ dll
- Web browser : Firefox,Chrome,Microsoft edge dll

- ### HTML Structure 
  Untuk membuat sebuah struktur awal HTML pada sebuah code editor visual studio code kalian bisa menggunakan (!) dan (doc)

- ### Tag dasar HTML
  HTML memiliki dua jenis tag yaitu single tag dan double tag

- ### Single tag
- untuk menampilkan gambar `<img/>`
- untuk menambahkan field inputan `<input/>`
- untuk menghubungkan file file `<link/>`

- ### Double tag
- Untuk membuat sebuah heading kita dapat menggunakan tag    `<h1>__</h1>`
- Untuk membuat sebuah paragraph kita dapat menggunakan tag  `<p>__</p>`
- Untuk membuat sebuah order list kita dapat menggunakan tag `<ol>__</ol>`
- Untuk membuat sebuah table kita dapat menggunakan tag      `<table>__</table>`
- Untuk membuat sebuah form kita dapat menggunakan tag       `<form>__</form>`

- ### Semantic HTML
  menggunakan element HTML yang sesuai dengan kebutuhan konten
  
- ### Tag Semantic HTML
- `<header>__</header>`
- `<nav>__</nav>`
- `<section>__</section>`
- `<article>__</article>`
- `<main>__</main>`
- `<aside>__</aside>`
- `<footer>__</footer>`

- ### Deploy HTML
  Deploy adalah sebuah proses kita mempublish halaman html kita ke server agar orang lain dapat mengaksesnya untuk layanan deploy sendiri ada banyak sekali platform gratis seperti : Github pages,Netlify,Heroku dll.
  
## CSS

