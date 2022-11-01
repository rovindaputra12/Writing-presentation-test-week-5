# **Writing & Presentation Week 5**

## **Web Server**<hr>

1. Web Server merupakan komponen penting dari Hardware dan Software.
   - Lalu dalam hardware tersebut digunakan untuk menyimpan software ke web server dan komponen situs web lainnya. Untuk mendukung pertukaran dengan perangkat lain maka dibutuhkan jaringan yang terhubung ke internet.
   - Lalu dalam perangkat lunak, web server digunakan untuk mengontrol penggunaan web yang sedang di hosting dengan menggunakan server HTTP yang menjalankan alamat web atau url dan diakses melalui web yang disimpan lalu dikirimkan ke konten situs web yang di hosting.
2. Metode - metode request :
   - Cara Traditional <br>
     Merupakan dimana web browser meminta data ke server yang di deploy(netlify) melewati API. Meminta sebuah data API dan dikembalikan yang sama.
   - Single page application / client site render <br>
     Merupakan saat membuka aplikasi dari web browser ke server dengan bentuk JSON.
   - Dinamic site
     Dimana proses yang dilakukan pada full di bagian server. Yang dapat diberikan dalam bentuk html atau json. Framework yang digunakan seperti laravel, express, next, nuxt.
   - Static site

## **Restful API**<hr>

1. REST (Representational State Transfer) dibuat pada tahun 2000.
2. Rest API Architectural Styles <br>
   - Organized in terms of : Compliance with six architectural contraints.
   - Format : XML,JSON,HTML, dan PlainText
   - Learning Curve : Easy
   - Community : Large
   - Use Case :
     - Public APIs
     - Simple Resource-Driven apps
3. Rules milik Rest yang harus dimiliki ;

   - Uniform Interface : Mudah dipelajari, sama bentuknya dengan API
   - Client Server : Web browser sebagai client, server untuk buat API
   - Stateless : Tidak tergantung oleh data user
   - Cacheable
   - Layered System
   - Codeon demand : sifat (optional)

4. RestFul = WEB API dengan rest memiliki 6 prinsip diatas.
5. HTTP = Komunikasi web dengan server dengan API sebagai jalur yang menjalankan http/ssh.
6. HTTP Nethod ;
   - Get -> Ambil data
   - Post -> Kirim data
   - Delete -> Hapus data
   - Put/Patch -> Put untuk update data sebagian atau semua data, Patch untul update hanya sebagian saja.
7. API bisa dikonsumsi oleh Mobile/web/dekstop/IOT.
8. Database hanya bisa diakses oleh server, Lalu API hanya bisa akses sampai di server.
9. Menggunakan kebabcase(-) bukan(\_)
10. Status Code
    - 2xx -> Sukses
    - 3xx -> Redirect
    - 4xx -> Client Eror -> disebabkan oleh pengguna
    - 5xx -> Server Eror -> disebabkan oleh server

## **Node JS**<hr>

1. Node js merupakan runtime javascript yang digunakan oleh back-end developer yang dibangun di JS engine yang bernama V8, lalu V8 tersebut dari web browser Chrome.
2. Runtime = menjalankan / meng eksekusi kode yang dibuat.
3. Ditemukan oleh Ryan Dahl (2009)
4. Build in module Node JS
   - Console
   - Process
   - OS
   - File System
   - Events
   - Util
5. Menginstal package/library `npm init` atau `npm i [nama package]`
6. Membuat web Server <br>
   ```javascript
       let a = require(`http`);
       a.createserver((req, res) => {
       res.write(`hallo`);
       res.end(); // untuk menghentikan respon agar tidak terjadi stuck
       });
        .listen(/*port*/, () => {
        console.log("data berhasil");
       });
   ```
7. `createserver` sebagai ngembaliin instance dari server.
8. `.listen` ngejalanin server dan mulai connect/aktif.

## **Express Js Routing dan Middleware**<hr>

1. Express merupakan framework untuk back-end atau web server yang dibangun di node js melalui jalur API.
2. Framework node = `npm isntall express`
3. Framework untuk development `npm install nodemon`
4. Middleware merupaka sebuah function yang bisa digunakan untuk memodifikasi Object Request & Object Response.
5. Nodemon digunakan untuk development sebagai running program di node js.
6. Menggunakan express js : <br>

   - Buka vscode, new terminal `npm init`
   - instal expreess js `npm instal express`
   - buat file idx.js,

     ```javascript
     const express = require("express");
     const idx = express();
     const PORT = 7000;

     //  running port
     idx.listen(PORT, () => {
       console.log("running port " + PORT);
     });

   - instal nodemon untuk development `npm i -D nodemon` lanjut dengan `npm run dev` untuk menjalankan nodemon.

## **Design Database with MySQL**<hr>

1. Database atau basis data adalah kumpulan informadi yang disimpan di dalam komputer secara sistematik sehingga dapat diperiksa menggunakan suatu program komputer untuk memperoleh informasi dari basis data tersebut.
2. Databaes memiliki fungsi : <br>

   - Mengelompokkan data dan informasi sehingga lebih mudah dimengerti.
   - Mencegah terjadinya duplikat data maupun inkonsistensi data.
   - Mempermudah proses penyimpanan, akses, pembaharuan, dan menghapus data.
   - Menjaga kualitas data dan informasi yang diakses sesuai dengan yang diinput.
   - Membantu proses penyimpanan data yang besar.
   - Membantu meningkatkan kinerja aplikasi yang membutuhkan penyimpanan data.

3. Manfaat menggunakan database : <br>

   - Tidak ada redudansi data, database dapat membantu meminimalkan redudansi data. Redundansi adalah munculnya banyak data dalam file yang berbeda.
   - Integritas data terjaga, database memastikan integritas data yang tinggi, di mana database akan memastikan keakuratan, aksesbilitas, konsistensi, dan kualitas tinggi pada suatu data.
   - Menjaga independensi data, database menjaga independensi data di mana orang lain tidak dapat mengubah data, meski data bisa diakses.
   - Kemudahan berbagi data, menggunakan perangkat lunak database bisa digunakan untuk berbagi data atau informasi dengan sesama pengguna lainnya.
   - Pemeliharaan keamanan data, database memastikan keamanan informasi dan data, di mana kamu dapat memasukkan kode akses untuk data tertentu yang tidak dapat diakses.
   - Kemudahan akses data, dengan adanya database kamu dapat mempermudah dalam mengakses dan memperoleh data karena semua data telah tertata dengan baik.

4. Di dalam design database ada attributes pada tiap entity nya.
5. Entity-relationship diagram (ERD) merupakan sebuah model untuk menyusun database agar dapat menggambarkan data yang mempunyai relasi dengan database yang akan didesain.
6. Di dalam ERD ada komponen-komponen seperti :

   - Entitas : Kumpulan objek yang dapat diidentifikasikan secara unik atau saling berbeda.
   - Atribut yang berfungsi untuk mendeskripsikan karakteristik dari entitas tersebut yang merupakan hal pembeda atribut dengan entitas. 
   - Relasi : Hubungan antara sejumlah entitas yang berasal dari himpunan entitas yang berbeda. Gambar relasi diwakili oleh simbol belah ketupat. <br> 

7. Membuat table <br>
   - Mahasiswa
     ```sql
     create table mahasiswa(
         -> Nim int,
         -> nama varchar,
         -> Jurusan varchar,
         -> PRIMARY KEY(Nim);
     ```
   - Matakuliah
     ```sql
     create table matakuliah(
         -> Id int,
         -> Matkul varchar,
         -> sks int,
         -> PRIMARY KEY(Id);
     ```