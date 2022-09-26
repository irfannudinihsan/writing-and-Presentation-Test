# Writing-and-Presentation-Test week 1

## Day 1 : Unix Command Line dan GIT & GITHUB

**Senin, 19 September 2022**

### Command Line Interface (CLI)

**Command Line Interface (CLI) : shell yang berbasis teks**

lalu shell itu apa? **Shell** adalah program yang menerima perintah lalu di eksekusi oleh system.

untuk mengakses CLI bisa menggunakan GIT

**cara mengakses CLI bagaimana?**
klik kanan logo windows > klik run > lalu ketikan cmd > klik ok

![cli](cli/cli.png)

### File System

**File system** adalah sebuah sistem yang mengatur/mengelola sebuah data dan direktori, dan file system menggunakan struktur berbentuk tree

**perintah-perintah di Command Line Interface (CLI)**

- pwd : perintah untuk melihat direktori saat ini

  ![ls](cli/pwd.png)

- ls : perintah untuk melihat isi direktori

  ![ls](cli/ls.png)

- cd : perintah untuk pindah direktori

  ![ls](cli/cd.png)

- mkdir : perintah untuk membuat direktori

  ![ls](cli/mkdir.png)

- touch : perintah untuk membuat file

  ![ls](cli/touch.png)

- cat : perintah untuk melihat isi file

  ![ls](cli/cat.png)

- cp : perintah untuk copy/salin

  ![ls](cli/cp.png)

- mv : perintah untuk pindah file/direktori

  ![ls](cli/mv.png)

- rm : perintah untuk menghapus file/direktori

  ![ls](cli/rm.png)

### **GIT & GITHUB**

**GIT** adalah version control system yang digunakan untuk mengelola sebuah file/direktori dan melakukan pencatatan ketika ada perubahan

**GITHUB** adalah layanan GIT yang digunakan programmer untuk mengelola file yang berbasis cloud dengan cara dihosting dan **GITHUB** juga dapat digunakan untuk kolaborasi.

#### **Kondisi-kondisi di GIT**

- modified : kondisi sudah ada perubahan tetapi masih untracked atau belum ditandai dan belum disimpan di version control system
- staged : kondisi kondisi sudah ada perubahan tetapi belum disimpan di version control system
- comitted : kondisi sudah ada perubahan dan sudah disimpan di version control system

#### **Perintah-perintah di GIT**

##### - **setup GIT**

- setup awal

  ![ls](git_github/setup.png)

##### - **kelola repository GIT**

- git init : perintah untuk menginisialisasi repository

![ls](git_github/init.png)

- git status : perintah untuk melihat kondisi

![ls](git_github/status.png)

- git add : perintah untuk menambahkan kondisi di staging

![ls](git_github/add.png)

- git commit : perintah untuk menyimpan perubahan di version control system

![ls](git_github/commit.png)

- git log : untuk melihat riwayat perubahan

![ls](git_github/log.png)

- git checkout : perintah yang digunakan untuk pindah perubahan

![ls](git_github/checkout.png)
- git branch : perintah untuk mebbuat jalur lain tanpa menggangu master

![ls](git_github/branch.png)

**Cara kerja GITHUB**
Programmer melakukan pengelolaan file/direktori di lokal, ketika akan melakukan upload dan bisa diakses secara publik prgrammmer akan melakukan perintah GIT/GITHUB secara CLI maupun GUI untuk upload di platform **GITHUB**

##### - **cara upload dit GITHUB**
1. buat repository baru di github
2. hubungkan repository local dengan repository github

![ls](git_github/remote.png)


3. upload file/direktori di local ke repository github

![ls](git_github/push.png)

## Day 2 : HTML 
**Selasa, 20 September 2022**
### **Hypertext Markup Language (HTML)**
#### Hypertext Markup Language (HTML) : bahasa markup yang digunakan sebagai struktur web

##### **Sturktur HTML**
Struktur HTML adalah kerangka kerja yang dimiliki HTML untuk menuliskan kode agar lebih terstruktur
- doctype : deklarasi untuk sebuah file dengan type HTML
- html : untuk menginformasikan yang diakses oleh browser yaitu file html
- head : tempat untuk meletakkan berbagai informasi pada html
- body : tempat menuliskan kode pada file html

##### **Anatomy HTML**
Anatomy HTML : susunan terurut dari HTML contohnya element, tag, content

##### **Element HTML**
Element adalah komponen yang menyusun dokumen HTML yang terdiri dari opening tag, content, closing tag.
 ``` 
- <p> paragraf </p> : tag paragraf
- <h1> heading </h1> : tag heading
- <img> : tag image
 ``` 

##### **Atribute HTML**
Atribute adalah tambahan styling untuk element HTML

##### **Cara kerja HTML**
HTML dapat berjalan dan dapat diakses melalui browser

lalu bagaimana cara menjalankan **HTML**? untuk menjalankannya harus menggunakan tools, berikut :
##### **tools cara menjalankan HTML**
-text editor (VScode, Sublime text, vim, notepad++)
-browser (chrome, mozilla, Microsoft Edge)

##### **Membuat file HTML**
 1. membuat file HTML menggunakan text editor (Visual Studio Code) dengan format ektensi HTML
 2. membuat sturktur HTML doctype,html,head,body
    ``` 
    <!DOCTYPE html>
    <html lang="en">
    <head>
    <title>praktikum</title>
    </head>
    <body>

    </body>
    </html>
    ```
3. menambahkan element HTML, atribute HTML, semantic HTML
    ``` 
    <!DOCTYPE html>
    <html lang="en">
    <head>
    <title>praktikum</title>
    </head>
    <body>
    <section id="profile">
      <h1>nama : Irfannudin Ihsan</h1>
    </section>

    <section id="contact-me">
      <h2>contact me</h2>

      <form action="">
        <div class="input">
          <label for="">name</label>
          <input type="text" name="" id="" />
        </div>

        <div class="input">
          <label for="">email</label>
          <input type="email" name="" id="" />
        </div>
        <button>send</button>
      </form>
    </section>
    </body>
    </html>
    ``` 

## Day 3 : CSS 
**Rabu, 21 September 2022**
### **Cascading Style Sheet (CSS)**
#### Cascading Style Sheet (CSS) : bahasa styling yang digunakan untuk memberikan warna,bentuk,font dan lainnya pada website.

##### **cara menggunakan/menyisipkan CSS**
- inline : menyisipkan di tag html
- internal : menyisipkan di dalam file html tepatnya pada head html
- external : menggunakan file lain dengan cara menyisipkan link yang mengarah css file

##### **Struktur CSS**
CSS memiliki bebrapa struktur untuk dapat memberi styling pada HTML
- selector : fungsi yang digunakan memilih tag html untuk diberikan styling
- property : fungsi apa yang diterapkan pada tag html
- value : isi dari yang di berikan pada tag html

    ``` 
      h1 {
    color : red;
    }
    ```
##### **CSS class name & id name**
- class name : sebagai penanda secara global untuk akses css
    ``` 
      <h1 class="heading">nama : Irfannudin Ihsan</h1>
    ``` 

- id name : sebagai penanda secara khusus untuk akses css
    ``` 
    <p id="paragraf">paragraf</p>
    ``` 
**contoh penerapan menggunakan CSS**
screenshot

##### **Multiple CSS**
cara menuliskan banyak selector dalam satu penulisan
``` 
h1, p, .heading {
    color : red;
    }
``` 

##### **Flexbox**
Flexbox adalah cara yang digunakan CSS untuk mengatur CSS layouting atau tata letak.
Flexbox mempunyai beberapa komponent yaiatu container dan items
- container : component yang membungkus atau menampung didalamnya
- items : component yang mewakili suatu konten yang ada didalamnya

##### **Flex-Direction**
Flex Direction adalah mengatur arah dari  items
- row : mengatur arah items secara horizontal
- row-reverse mengatur arah items dengan uruatan terbalik secara horizontal
- column : mengatur arah items secara vertikal
- column : mengatur arah items dengan urutan terbaik secara vertikal

## Day 4 : Algoritma 
**Kamis, 22 September 2022**
### **Algoritma**
#### Algoritma : langkah-langkah meneyelesaikan masalah secara logis dan sistematis.

##### **Manfaat Algoritma**
Manfaat dari algoritma yaitu membantu dalam menyelesaikan masalah dengan secara terurut dan menjadi podasi membuah sistem dengan bahasa pemrograman 


##### **ciri-ciri Algoritma**
- input : sebuah variabel yang berisi nilai untuk proses sistem
- output : keluaran nilai yang di proses sistem
- Definiteness : Instruksi yang jelas untuk proses
- Finiteness : merupakan titik berhenti untuk proses
- Effectiveness : proses yang tepat yang efisien

##### **Jenis Proses Algoritma**
- Sequence : Intruksi yang berjalan secara terurut
- Selection Intruksi yang dijalankan untuk menyelesaikan kondisi tertentu
- Iteration : Intruksi yang berjalan berulang ketika kondisi memenuhi
- Concurrent : Instruksi yang berjalan secara bersamaan

##### **Penyajian Algoritma**
- Deskriptif : Penulisan algoritma secara deskriptif atau dengan cara menjabarkan dengan bahasa sehari-hari
- Flowchart : Penulisan algoritma dengan diagram alur dengan setiap proses diwakili dengan simbol-simbol
- Pseudocode : Penulisan algoritma seperti penulisan bahasa pemrograman tetapi dengan bahasa yang mudah dipahami

##### **Contoh Algoritma**
**Pseudecode**
Mencari angka genap
deklarasi
angka = 0
angka < 20
deskripsi
    if angka % 2 == 0
end

##### **Contoh penerapan algoritma dengan cara JavaScript**
mencari angka genap dari 0 sampai 20
``` 
    for (angka = 0; angka < 20; angka++) {
    if(angka % 2 == 0) {
        console.log(` ini bilangan genap : ${angka}`)
        }
    }
``` 