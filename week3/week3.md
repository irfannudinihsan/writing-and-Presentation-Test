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
* 
    **membuat dan cara akses**
    ```
    let siswa = [
  ["Irfan", "Yogyakarta", 21],
  ["Nudin", "Sleman", 20],
  ["Ihsan", "Bantul", 23],
    ];
    console.log(siswa[1][2]);
    ```

    