# Writing-and-Presentation-Test week 4

## Day 1 : Async Await

**Senin, 10 Oktober 2022**

#### **Async Await**

- **Array** adalah sebuah proses Asynchronous pada ES2017 untuk mempermudah mengangani promise agar penulisan code lebih efisien.
- **Contoh Async Await**
  ```
  let nonton = (kondisi) => {
    return new Promise((resolve, reject) => {
      if ((kondisi = "jalan")) {
        resolve("nonton terpenuhi");
      } else {
        reject("gak jadi");
      }
    });
  };

  async function asyncNonton() {
    try {
      let result = await nonton("jalan");
      console.log(result);
    } catch (eror) {
      console.log(eror);
    }
  }
  asyncNonton();
  ```
- **Contoh Async Await mengmbil data dari API**
  ```
  let containerDigimon = document.getElementById("list-digimon");
  let getDataDigimon = async () => {
    let response = await fetch("https://digimon-api.vercel.app/api/digimon");
    let digimons = await response.json();

    digimons.forEach((item) => {
      containerDigimon.innerHTML += `<h3> ${item.name} </h3> <img src="${item.img}"> <p> ${item.level} </p> `;
    });
  };
  getDataDigimon();
  ```

## Day 2 : Git & Github Lanjutan

**Selasa, 11 Oktober 2022**

#### **Git & Github Lanjutan**

- **Git Branch (perintah untuk membuat jalur baru untuk eidt file tanpa mengganggu jalur utama/main atau master)**
  ```
  git branch A-login
  ```
- **Git Switch (perintah untuk pindah branch)**
  ```
  git switch A-login
  ```
- **Git Merge (perintah untuk menggabungkan branch)**
  ```
  git merge dev
  ```
- **Pull Request (perintah untuk meminta menambahkan repo dari lokal ke repository)**
  ```
  git pull origin dev
  ```

  ## Day 3 : Responsive Web Design
**Rabu, 12 Oktober 2022**

#### **Responsive Web Design (CSS)**
- **Responsive Web Design adalah sebuah perilaku tampilan web yang menyesuaikan ukuran pada device yang digunakan**

- **Viewport dalam HTML adalah mengoptimalkan sebuah website untuk menyesuaikan pada tampilan device**
     ```
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
     ``` 
- **CSS Unit adalah satuan ukuran pada pada CSS untuk mengatur element pada HTML**
    - px
    - em
    - rem
    - cm
    - max-width
    - % (persen)

- **Media Query adalah cara untuk mengatur ukuran ukuran sebuah tampailan web**
    ```
    @media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
        }
    }
     ``` 
 - **Breakpoint adalah batasan-batasan ukuran pada tampilan web**
    ```
    /* Extra small devices (phones, 600px and down) */
    @media only screen and (max-width: 600px) {
      .example {background: red;}
    }
    
    /* Small devices (portrait tablets and large phones, 600px and up) */
    @media only screen and (min-width: 600px) {
      .example {background: green;}
    }
    
    /* Medium devices (landscape tablets, 768px and up) */
    @media only screen and (min-width: 768px) {
      .example {background: blue;}
    } 
    
    /* Large devices (laptops/desktops, 992px and up) */
    @media only screen and (min-width: 992px) {
      .example {background: orange;}
    } 
    
    /* Extra large devices (large laptops and desktops, 1200px and up) */
    @media only screen and (min-width: 1200px) {
      .example {background: pink;}
    }
     ``` 

#### **Responsive Web Design (Bootstrap)**
- **Bootstrap adalah framework yang berbasis HTML, CSS, Javascript yang membantu dalam mempermudah dalam mendesain tampilan website**

 - **Installasi Bootstrap (installasi bootstrap secara online dengan Content Deliver Network)**
    ```
    <!DOCTYPE html>
    <html lang="en">
      <head>
        <title>Document</title>
        <!-- CDN Bootstrap -->
        <link
          href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css"
          rel="stylesheet"
          integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi"
          crossorigin="anonymous" />
      </head>
      <body>
        
      </body>
    </html>
    ```
 - **Container Bootstrap adalah tag sebagai wadah untuk menampung element (penulisan container menggunakan class="container")**
    ```
     <!-- Container -->
    <div class="container">
     <p> kontent dalam kontainer </p>
    </div>
    
     <!-- Container fluid -->
    <div class="container-fluid">
     <p> kontent dalam kontainer </p>
    </div>
    ```
 - **Grid System adalah sistem kerangka kerja dua dimensi untuk menyelaraskan dan meletakkan elemen desain, di dalam grid terdapat row(baris) dan col(kolom) untuk mengatur layouting**
    ```
        <div class="container text-center">
      <div class="row">
        <div class="col">
          Column
        </div>
        <div class="col">
          Column
        </div>
        <div class="col">
          Column
        </div>
      </div>
    </div>
    ```
    
 - **Grid Option adalah grid system yang mengatur ukuran dengan breakpoint dengan aturan dari Bootstrap**

![breakpoint1](/breakpoint1.png)
![breakpoint2](/breakpoint2.png)

    ```
    <div class="container text-center">
      <div class="row">
        <div class="col-sm-8">col-sm-8</div>
        <div class="col-sm-4">col-sm-4</div>
      </div>
     <div class="row">
        <div class="col-sm">col-sm</div>
        <div class="col-sm">col-sm</div>
        <div class="col-sm">col-sm</div>
      </div>
    </div>
    ```