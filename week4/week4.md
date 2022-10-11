# Writing-and-Presentation-Test week 4

## Day 1 : Async Await

**Senin, 3 Oktober 2022**

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

**Senin, 3 Oktober 2022**

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
