
# Writing-and-Presentation-Test week 7
## Day 1 : MySQL Basic
**Senin, 31 Oktober 2022**
#### **Database**
- **Database** adalah kumpulan data dan informasi yang disimpan didalam komputer secara sistematik dan saling berelasi.
- **Database Management System** adalah software yang digunakan user untuk berkomunikasi dengan data yang ada di dalam penyimpanan.
- **Table** adalah kumpulan nilai data yang terdiri dari kolom dan baris. Di dalamnya berisikan atribut dari sebuah data.
-**Field** adalah kolom dari table dimana masing-masing field memiliki tipe data.
-**Record** adalah isi nilai dari sebuah tabel.
#### **SQL**
- **Structured Query Language (SQL)** adalah bahasa query yang digunakan mengelola database dan interaksi di Relational Database Management System.
- **MySQL** adalah RDBMS open-source berbasis SQL yang bekerja dengan model client-server.
- **Tipe Data SQL**
    - Number : int, float, decimal
    - String : char, varchar, text, enum
    - Boolean : true, false
    - Date Time : date, datetime, time, timestamp

- **DDL (Data Definition Language) : perintah SQL yang digunakan untuk berinteraksi dengan struktur dan definisi metadata dari objek-objek database.**
    - membuat table pada database
    ``
    create database favorite_movie;
    ``

     - Alter berfungsi untuk mengubah struktur tabel
    ``
    alter table student add jurusan varchar(25);
    ``
    
     - Drop berfungsi untuk menghapus tabel
    ``
    drop table student;
    ``
    
- **Data Manipulation Language (DML) : perintah SQL yang digunakan untuk berinteraksi dengan data data yang ada dalam database.**
    - SELECT berfungsi untuk memilih data yang ingin ditampilkan
        ``
        select * from movie;
        ``

    - INSERT berfungsi untuk memasukan data ke dalam tabel
        ``
        insert into student (nama, email, jurusan) values
("irfan", "irfan@gmail.com", "teknik informatika"),
("nudin", "nudin@gmail.com", "sistem informasi"),
("ihsan", "ihsan@gmail.com", "teknik komputer");
        ``
    - WHERE, AND, OR, NOT, LIKE digunakan untuk memberikan syarat dalam menampilkan data
        ``
        SELECT * FROM students
        WHERE id >= 6 AND age >= 21 OR age < 24 NOT id > 4
        SELECT * FROM mahasiswas WHERE name LIKE "%udin";
        ``
        
        - UPDATE berfungsi untuk edit pada data
        ``
        update student set nama = "udin" where id = 2;
        ``
        
        - DELETE berfungsi untuk menghapus sebuah data
        ``
        delete from movie where id = 1;
        ``