# Writing-and-Presentation-Test week 2

## Day 1 : Function, Scope, Looping
**Senin, 26 September 2022**

##### **For loop**
Untuk membuat looping for loop memiliki sturktur yaitu for(intial,condition, iteration)
```
for (let i = 1 ; i <= 10 ; i++) {
    if(i == 6) {
        console.log(`${i} : yess `)
    } else {
        console.log(i)
    }
}
```

##### **While**
while adalah proses perulangan suatu blok kode program selama sebuah kondisi terpenuhi
```
while (!isKetemu) {
  if (i % 2 == 0 && i % 3 == 0 && i % 4 == 0 && i % 5 == 0 && i % 6 == 0) {
    console.log(i);
    isKetemu = true
  }
  i++
}
```

##### **Function & Scope**
Function : Suatu code yang menjalankan perintah tertentu
Scope : Suatu alur variabel yang menentukan posisinya dapat diakses pada jangkauan tertentu
```
function greeting(name) {
  console.log(`halo, namaku ${name}`);
}
greeting("irfan");
```

##### **For & Function**
```
function cariAngka (x) {
    let isKetemu = false;

    for(let i = 1; i <=20 ; i++) {
        if (i == x) {
            console.log(i);
            isKetemu = true
        } else {
            console.log('data tidak ditemukan')
        }
    }
}
cariAngka(3)
cariAngka(15)
cariAngka(21)
```


## Day 2 : Data Type Built in Prototype & Method
**Selasa, 27 September 2022**

##### **Data Type**
Data Type/ Tipe data : pengklasifikasian sebuah data berdasarkan jenis data
Tipe data di Javascript string,number,boolean, object
```
let nama = "irfan";
let umur = 21;
let sudahMakan = true;
let data = {
    nama : "irfan",
    umur : 21,
    sudahMakan : true,
}
```
##### Tipe data primitive vs Non-primitive
primitive : tipe data yang hanya mempunya value tanpa punya properti atau method
- Numbers
- Strings
- Booleans
- undefined
- null

non-primitive : tipe data yang hanya mempunya value, punya properti atau method
- Objects
- Arrays
- Functions

##### **Built in Prototype and Method**

Built in adalah sebuah properti method yang digunakan menyelesaikan sebuah nilai
```
let hewan = 'HaRimau';
console.log( typeof hewan);
console.log(hewan.length);
console.log(hewan.toLocaleUpperCase);
console.log(hewan.charAt(2));


let nomor = 1234;
console.log(isNaN(nomor));
console.log(nomor.toString());

console.log(Math.PI);

let pi = 3.1445654
console.log(pi.toFixed(2))
```

## Day 3 : Document Object Model
**Rabu, 28 September 2022**

##### **DOM**
Document Object Model : dokument atau HTML yang di modelkan dalam sebuah objek
Di dom dapat memanipusi element dan node
- Element adalah tag HTML
- Node adalah kontent didalam

##### **Traversing**
Traversing adalah cara-cara mengakses dan melintasi DOM
- Traversing ke bawah
```
document.getElementById('paragraf');
document.getElementsByClassName('konten');
document.querySelector('#item1');
document.querySelectorAll('.item');
```

- Traversing ke Atas
```
console.log(itemQuery.parentElement);
```

- Traversing ke Samping
```
console.log(itemQuery.nextElementSibling);
console.log(itemQuery.previousElementSibling);
```


## Day 4 : Manipulation DOM
**Kamis, 29 September 2022**

Memanipuasi DOM : mengakses dokumen yang berada pada HTML dan mengeditnya dengan DOM

Membuat dan menambahkan Element
```
let app = document.getElementById('app');
app.innerHTML = "<h1> Haii </h1>";
let p1 = document.createElement("p");
P1.innerHTML = "<h1> hai </h1>";

app.appendChild(p1)
```

Menghapus
```
let end = document.getElementById("end");
end.remove();
```
Menambahkan attribute dan style
```
let link = document.getElementsByClassName("link")[0]
link.setAttribute("id", "google");
link.style.color = 'yellow';
link.style.backgroundColor = 'blue';
```
## Day 5 : Event DOM
**Jumat, 30 September 2022**
Event DOM adalah interaksi user pada document HTML yang dilakukan oleh object model

##### **Macam-macam jenis event DOM**
- Click
- Scroll
- Change
- Focus
- Hover
- Submit
- Blur

##### **Menangkap Interaksi dari event DOM**
- Element.addEventListener
- Element.onevent


##### **Event DOM dengan addEventListener**
```
let button = document.getElementById("btn");

button.addEventListener("click", function () {
  alert("ini button");
});
```
##### **Studi Kasus Event DOM pada form**
```
let loginForm = document.getElementById("sign-in");
let inputUsername = document.querySelector("#username");
let inputPassword = document.querySelector("#password");

let user = {
    username : 'irfan',
    password : '123',
}

loginForm.addEventListener("submit", (event) => {
  event.preventDefault();

  let userLogin = {
    username: inputUsername.value,
    password: inputPassword.value,
  };

 console.log(userLogin);

 let login = userLogin.username == user.username &&
             userLogin.password == user.password;

    if(login) {
        console.log('berhasil login');
    } else {
        console.log('gagal login');
    }
  loginForm.reset();
});
```
