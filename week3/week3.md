# Writing-and-Presentation-Test week 3

## Day 1 : Array & Array Multidimensional

**Senin, 3 Oktober 2022**

#### **Array**

- **Array** adalah tipe data non-primitive yang dapat menyimpan berbagai macam tipe data seperti string, number, boolean dan lainnya.

- **Contoh Array** (membuat array dan mengakses arrray)
  ```
  let daftarMakanan = [
      'mieayam',
      'bakso',
      'soto',
      'sate',
  ];
  console.log(daftarMakanan[2]);
  ```
- **Update Array (memberikan perubahan data pada array)**

  ```
  let daftarMakanan = [
      'mieayam',
      'bakso',
      'soto',
      'sate',
  ];
  daftarMakanan[3] = 'bubur';
  console.log(daftarMakanan);
  ```

- **Const Array (array dengan const tidak bisa update data, tetapi bisa update nilai konten)**
  ```
  const motor = ['honda','yamaha', 'suzuki']
  motor[2] = 'kawasaki';
  console.log(motor);
  ```

* **Array Properties adalah properti yang digunakan pada array seperti length, construktor, index.input, prototype**
  ```
      const motor = ['honda','yamaha', 'suzuki']
  console.log(motor.length);
  ```
* **Array Method adalah sebuah fungsi built-in yang memudahkan dalam menangani array**
  **push**

  ```
  let buah = [
     'mangga',
     'semangka',
     'jeruk'
  ]

  buah.push('nanas');
  console.log(buah);
  ```

  **pop**

  ```
      let buah = [
          'mangga',
          'semangka',
          'jeruk'
      ]
      buah.pop();
      console.log(buah);
  ```

  **shift**

  ```
      let buah = [
          'mangga',
          'semangka',
          'jeruk'
      ]
      buah.shift();
      console.log(buah);
  ```

  **unshift**

  ```
    let buah = [
  'mangga',
  'semangka',
  'jeruk']
  buah.unshift('anggur');
  console.log(buah);
  ```

* **Looping pada array menggunakan for, map dan forEach**

  **for**

  ```
  let buah = [
  'mangga',
  'semangka',
  'jeruk'
  ]

  for ( let i = 0; i < buah.length; i++ ) {
      console.log(buah[i]);
  }

  //for in
  let buah = ["mangga", "semangka", "jeruk"];

  for (let buahku in buah) {
    console.log(buahku);
  }
  ```

  **forech (looping pada setiap elemen array)**

  ```
  let buah = ["mangga", "semangka", "jeruk"];

  buah.forEach((buahku) => {
    console.log(buahku);
  });
  ```

  **forech (looping pada setiap elemen array)**

  ```
  let buah = ["mangga", "semangka", "jeruk"];

  buah.forEach((buahku) => {
    console.log(buahku);
  });
  ```

  **map (looping dengan membuat array baru)**

  ```
  let buah = ["mangga", "semangka", "jeruk"];

  buah.map((item) => {
    console.log(item);
  });
  ```

* **Array Multidimensional adalah data array didalam array**
* **membuat dan cara akses**
  ```
  let siswa = [
  ["Irfan", "Yogyakarta", 21],
  ["Nudin", "Sleman", 20],
  ["Ihsan", "Bantul", 23],
  ];
  console.log(siswa[1][2]);
  ```

## Day 2 : Object

**Selasa, 4 Oktober 2022**

#### **Object**

- **Object** adalah sebuah tempat yang data yang memiliki struktur proterti dan nilai, properti seperti nama yang menampung niali. Di Object juga memiliki method.

- **Mebuat Object dan mengakses**
  ```
  let hewan = {
  nama: "kucing",
  kaki: 4,
   warna: "putih",
  };
  console.log(hewan.nama);
  ```
- **Update Object**

  ```
  let hewan = {
  nama: "kucing",
  kaki: 4,
  warna: "putih",
  };
  hewan.warna = "hitam";
  console.log(hewan);
  ```

- **Delete in Object**
  ```
  let hewan = {
  nama: "kucing",
  kaki: 4,
  warna: "putih",
  };
  delete hewan.warna;
  console.log(hewan);
  ```
- **Method adalah sebuah fungsi yang terdapat di dalam method yang dijalan dengan cara dipanggil dengan nama objecy lalu nama methodnya**

  ```
  const greeting = {
  welcome: function () {
  return "halo gaess";
  }
  };
  console.log(greeting.welcome());
  ```

- **Nested Object adalah object yang terdapat didalam object**
  ```
  let buku = {
  judul: "tips jago javascript",
  tahun: 2022,
  penulis: {
  penulis1: {
    nama: "reyhan",
    umur: 21,
    kota: "jakarta",
  },
  penulis2: {
    nama: "udin",
    umur: 22,
    kota: "Bandung",
  },
  },
  };
  console.log("nama penulis1" , buku.penulis.penulis1.nama);
  ```
- **Looping Object adalah menmpilkan seluruh data pada object dengan looping for dan key sebagai index**

  ```
  let buku = {
    judul: "tips jago javascript",
    tahun: 2022,
    penulis: {
      penulis1: {
        nama: "reyhan",
        umur: 21,
        kota: "jakarta",
      },
      penulis2: {
        nama: "udin",
        umur: 22,
        kota: "Bandung",
      },
    },
  };
  ```

- **Array Object**
  ```
  let users = [
  {
  nama: "irfan",
  umur: 21,
  alamat: "bandung",
  },
  {
  nama: "nudin",
  umur: 22,
  alamat: "jakarta",
  },
  {
  nama: "ihsan",
  umur: 29,
  alamat: "bali",
  },
  ];
  ```

## Day 3 : JavaScript Modules & Recursive

**Rabu, 5 Oktober 2022**

#### **JavaScript Modules**

- **JavaScript Modules** cara memisahkan kode ke file yang berbeda dengan perintah export import

- **Cara melakukan export import**
  - Index
  ```
  <body>
  <script src="./indonesia.js" type="module"></script>
  </body>
  ```
  - Import
  ```
  import { motor } from "./jepang";
  ```
  - Export
  ```
  export let motor = ["suzuki", "honda", "kawasaki","toyota","yamaha"];
  ```

#### **Recursive**

- **Recursive** sebuah fungsi yang memmanggil dirinya sendiri sampai dalam kodisi tertentu.

- **Recursive mencari deret angka**
  ```
  function deretAngka(n) {
  if (n == 1) {
      console.log(n)
  } else {
      deretAngka(n-1)
      console.log(n)}
  }
  deretAngka(6)
  ```

## Day 4 : Asynchronous

**Kamis, 6 Oktober 2022**

#### **JavaScript Asynchronous adalah sebuah konsep JavaScript yang memproses sebuah task dengan mengerjakan task lain tanpa menunggu selesai**

- **Callback**

```
   const p1 = () => {
     console.log("p1");
   };
   p1();

   const p2 = () => {
     setTimeout(() => {
       console.log("p2");
     }, 3000);
   };
   p2();

   const p3 = () => {
     console.log("p3");
   };

   p3();
```

- **Promise adalah sebuah cara proses data yang memiliki tiga ciri-ciri peding, fullfilled, reject**
  ```
  let makanPromise = new Promise((resolve, reject) => {
    makan = true;
    if (makan) {
      resolve("kenyang");
    } else {
      reject("lapar");
    }
  });

  makanPromise.then((result) => {
    console.log(result);
  });

  makanPromise.catch((err) => {
    console.log(err);
  });
  ```
- **Async await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise.**
  ```
  async function hello() {
    let result = await "hello";
    return result;
  }
  ```

## Day 5 : Asynchronous

**Jumat, 7 Oktober 2022**

#### **Web Storage adalah sebuah web API yang menyimpan data secara lokal**

- **Local Storage adalah tempat menyimpan di browser yang bisa digunakan untuk menyimpan data dan data tidak akan hilang walaupun browser di close dan komputer di restart.**
- **Session Storage adalah tempat menyimpan data hanya untuk satu sesi. Data dihapus ketika pengguna menutup tab browser tertentu.**
