
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
        
## Day 2 : MySQL Lanjutan
**Selasa, 1 November 2022**
#### **MySQL Lanjutan**
- **Relation di SQL** 
    - One to One : satu baris di tabel hanya dapat berhubungan dengan satu baris di tabel kedua.
    - One to Many : satu baris di tabel  dapat berhubungan dengan beberapa baris.
    - Many to Many : satu baris dapat berhubungan dengan beberapa baris dan baris yang berhubungan itu dapat berhubungan dengan baris lainnya.

- **Database Normalization**
    - **Database Normalization** adalah teknik analisis data yang mengorganisir atribut dengan mengelompokan sehingga terbentuk entitas yang non-redundant, stabil, flexsible.
    - **Bentuk Data Normalization**
        - First Normal Form (1NF)
            - setiap kolom bernilai tunggal
            - setiap kolom memiliki nama unik
            - ada primary key
        - Second Normal Form (2NF)
            - menggunkan 1NF
            -  tidak ada partial depedency(atribute yg tidak ada hubungan dengan primary key dipisah)
        - Third Normal Form (3NF)
            - menggunkan 1NF,2NF
            -  tidak ada transitif depedency (tidak ada atibute pada atribute lain, selain primary key)

    - **Primary Key adalah** nilai dalam data yang digunakan untuk mengidentifikasi suatu baris pada tabel.
     ``
        create table category (
        id int primary key not null auto_increment,
        nama varchar(25)
        );
    ``
    - **Primary Key adalah** nilai dalam data yang digunakan untuk menciptakan hubungan (relasi) antar tabel.
        ``
        create table product (
        id int primary key not null auto_increment,
        name varchar(50),
        price int,
        category_id int,
        foreign key (category_id) REFERENCES category(id));
        ``
    - **Join Multiple Table** adalah mengambil data dari dua atau lebih tabel yang memiliki relasi dan akan disajikan dalam single result set.
        - Inner Join
        ``
        select product.id, product.name, product.price, category.name
        from product inner join category
        on product.category_id = category.id;
        ``
        - Left Join
        ``
        select product.id, product.name, product.price, category.name
        from product left join category
        on product.category_id = category.id;
        ``
        - Right Join
        ``
        select product.id, product.name, product.price, category.name
        from product Right join category
        on product.category_id = category.id;
        ``
        - **Agrgregate Functions** adalah mengambi satu nilai setelah melakukan perhitungan pada sekumpulan nilai.
        - Max
        ``
        select name, max(price) from product;
        ``
         - Min
        ``
        select name, min(price) from product;
        ``
         - Sum
        ``
        select name, sum(price) from product;
        ``
         - Count
        ``
        select count(name) from product;
        ``
         - Price
        ``
        select avg(price) from product;
        ``