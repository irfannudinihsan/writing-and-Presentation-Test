## Day 1 : JavaScript 
**Kamis, 27 September 2022**
### **JavaScript Dasar**

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

##### **Function**
Suatu code yang menjalankan perintah tertentu
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
