# Writing-and-Presentation-Test week 1

## #Day 1 : Unix Command Line dan GIT & GITHUB

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
