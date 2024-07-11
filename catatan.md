# Catatan Ujian Fundamental Javascript
#### By: Jovi Rachman & Gemini 


## 1. Tipe Data
Javascript memiliki beberapa tipe data dasar, yaitu:

1. **Number**: Untuk nilai numerik (misalnya, 1, 3.14, -100)
2. **String**: Untuk nilai teks (misalnya, "Hello", "World!", "123")
3. **Boolean**: Untuk nilai true atau false (misalnya, true, false)
4. **Undefined**: Untuk nilai yang belum didefinisikan
5. **Null**: Untuk nilai yang secara eksplisit dikosongkan

Cara cek tipe data menggunakan **typeof**

```js

// Number
let age = 20;
console.log(typeof age); // Output: number

// String
let name = "John Doe";
console.log(typeof name); // Output: string

// Boolean
let isStudent = true;
console.log(typeof isStudent); // Output: boolean

// Undefined
let x;
console.log(typeof x); // Output: undefined

// Null
let y = null;
console.log(typeof y); // Output: object (Catatan: typeof null secara teknis mengembalikan "object" di Javascript)


```

## 2 & 13. Cara mengakses value dari suatu property/elemen di dalam suatu Object & Array
### Penjelasan:

1. **Object**: Digunakan untuk menyimpan kumpulan data yang terdiri dari pasangan kunci-nilai (key-value).

### Cara akses value dari suatu property atau elemen di **Object**
```js

let person = {
  name: "John Doe",
  age: 20,
  occupation: "Software Engineer"
};

console.log(person.name); // Output: John Doe
console.log(person["age"]); // Output: 20

```

2. **Array**: Digunakan untuk menyimpan kumpulan data yang terurut.

### Cara akses value dari suatu property atau elemen di **Array**
```js

let numbers = [1, 2, 3, 4, 5];

console.log(numbers[0]); // Output: 1
console.log(numbers[3]); // Output: 4

```

## 3. Built-in Method pada Array dan Object di Javascript
### Penjelasan:
Javascript menyediakan berbagai method built-in untuk Array dan Object yang dapat digunakan untuk memanipulasi data.

### Contoh Kode **Array**

 1. **push**: Menambahkan elemen baru ke akhir array.

```js

let numbers = [1, 2, 3];
numbers.push(4);
console.log(numbers); // Output: [1, 2, 3, 4]

```
 2. **pop**: Menghapus elemen terakhir dari array dan mengembalikannya.

```js

let numbers = [1, 2, 3];
let lastElement = numbers.pop();
console.log(numbers); // Output: [1, 2]
console.log(lastElement); // Output: 3

```
 3. **shift**: Menghapus elemen pertama dari array dan mengembalikannya.

```js

let numbers = [1, 2, 3];
let firstElement = numbers.shift();
console.log(numbers); // Output: [2, 3]
console.log(firstElement); // Output: 1

```
 4. **unshift**: Menambahkan elemen baru ke awal array

```js

let numbers = [1, 2, 3];
numbers.unshift(0);
console.log(numbers); // Output: [0, 1, 2, 3]

```
 5. **map**: Mengubah setiap elemen dalam array menjadi elemen baru.

```js

let numbers = [1, 2, 3];
let squaredNumbers = numbers.map(function(number) {
  return number * number;
});
console.log(squaredNumbers); // Output: [1, 4, 9]

```
 6. **filter**: Memfilter array dan hanya mengembalikan elemen yang memenuhi kondisi tertentu.

```js

let numbers = [1, 2, 3, 4, 5];
let evenNumbers = numbers.filter(function(number) {
  return number % 2 === 0;
});
console.log(evenNumbers); // Output: [2, 4]

```

### Contoh Kode **Object**

 1. **Object.keys**: Mengubah object menjadi array yang berisi semua propertinya.

```js

let person = {
  name: "John Doe",
  age: 20,
  occupation: "Software Engineer"
};

let keys = Object.keys(person);
console.log(keys); // Output: ["name", "age", "occupation"]

```
 2. **Object.values**: Mengubah object menjadi array yang berisi semua nilainya.

```js

let person = {
  name: "John Doe",
  age: 20,
  occupation: "Software Engineer"
};

let values = Object.values(person);
console.log(values); // Output: ["John Doe", 20, "Software Engineer"]

```
 3. **Object.entries**: Mengubah object menjadi array yang berisi array pasangan kunci-nilai.

```js

let person = {
  name: "John Doe",
  age: 20,
  occupation: "Software Engineer"
};

let entries = Object.entries(person);
console.log(entries); // Output: [["name", "John Doe"], ["age", 20], ["occupation", "Software Engineer"]]

```

## 4. Deklarasi Variable
### Penjelasan:
Javascript menyediakan berbagai keyword untuk mendeklarasikan variable.

### Contoh Kode

```js

// var (keyword lama)
var name = "John Doe";
console.log(name); // Output: John Doe

// let (keyword yang direkomendasikan)
let age = 20;
console.log(age); // Output: 20

// const (untuk nilai yang tidak dapat diubah)
const PI = 3.14159;
console.log(PI); // Output: 3.14159

```

## 5. Kondisi dan Operator Logika
### Penjelasan Kondisi:
Javascript menyediakan struktur kontrol if/else dan operator logika untuk membuat keputusan dan percabangan dalam kode.

### Penjelasan dan Contoh Kode **if**
1. **if**: digunakan untuk memeriksa 1 kondisi.

```js

let x = 10;
if (x > 5) {
    console.log("x lebih besar dari 5");
}

```
### Penjelasan dan Contoh Kode **if else**
2. **if else**: memeriksa satu kondisi dan menyediakan alternatif jika kondisi tersebut salah.

```js

let x = 3;
if (x > 5) {
    console.log("x lebih besar dari 5");
} else {
    console.log("x tidak lebih besar dari 5");
}

```

### Penjelasan dan Contoh Kode **if else if else**
3. **if else if else**: digunakan untuk memeriksa beberapa kondisi secara berurutan, dan menyediakan alternatif jika semua kondisi tersebut salah.

```js

let x = 7;
if (x > 10) {
    console.log("x lebih besar dari 10");
} else if (x > 5) {
    console.log("x lebih besar dari 5 tapi kurang dari atau sama dengan 10");
} else {
    console.log("x kurang dari atau sama dengan 5");
}

```

### Penjelasan Operator Logika
Operator Logika:

1. **&&**: **AND** (kedua kondisi harus benar) (salah satu ada **false** maka semua jadi **false**)
2. **||**: **OR** (salah satu kondisi harus benar) (salah satu ada **true** maka semua jadi **true**)
3. **!**: **NOT** (membalikkan kondisi) (berlawanan)

### Bisa di-open [Tabel Kebenaran](truth_table.png) 

## 6 & 14. Konsep Hoisting, fungsi apa saja yang bisa di hoist dan apa yang tidak bisa 
### Penjelasan:
**Hoisting** adalah mekanisme di mana deklarasi variable dan fungsi di JavaScript diproses sebelum kode dijalankan.

1. **Function Declaration** console.log nya bisa diatas function-nya
2. **Function Expressions** console.log nya tidak bisa diatas function-nya

### Contoh Kode dengan function declaration dan function expression
```js

// Memanggil fungsi sebelum didefinisikan
try {
    sayHello();
} catch (e) {
    console.log(e); // ReferenceError: sayHello is not defined
}

var sayHello = function() {
    console.log("Hello, world!");
};

// Memanggil fungsi setelah didefinisikan
sayHello(); // Output: "Hello, world!"

```

## 7. Built-in Method untuk memotong/mengambil sebagian value dari suatu array
### Penjelasan:
Javascript menyediakan method built-in ___splice___, ___slice___, dan ___replace___ untuk memotong/mengambil value array.

### Contoh Kode
1. **splice** 

```js

let numbers = [1, 2, 3, 4, 5];
numbers.splice(2, 2); // Menghapus dua elemen dari index 2 
console.log(numbers); // Output: [1, 2, 5]



```
2. **slice**

```js

let numbers = [1, 2, 3, 4, 5];
let subArray = numbers.slice(1, 4); // Mengambil elemen dari index 1 hingga 3 (tidak termasuk 4)
console.log(subArray); // Output: [2, 3, 4]

```
3. **replace**

```js

let text = "Hello, World!";
text.replace("World", "JavaScript"); // Mengganti "World" dengan "JavaScript"
console.log(text); // Output: Hello, JavaScript!

```

## 8 * 15. Cara penggunaan | += | -= | /= | *= | dan Decrement serta Increment variable Postfix & Prefix
### Penjelasan Aritmatika:
Javascript menyediakan berbagai operator aritmatika untuk melakukan operasi matematika.

### Contoh Kode

```js

let x = 10;
let y = 5;

console.log(x + y); // Output: 15
console.log(x - y); // Output: 5
console.log(x * y); // Output: 50
console.log(x / y); // Output: 2
console.log(x % y); // Output: 0 (sisa pembagian)
console.log(x ** y); // Output: 100000 (pangkat)

```

### Penjelasan Increment/Decrement
1. **++**: ___Increment___ (menambah 1)
2. **--**: ___Decrement___ (mengurangi 1)

### Contoh Kode

```js

let x = 10;

console.log(x++); // Output: 10 (nilai x sebelum increment)
console.log(x); // Output: 11

console.log(x--); // Output: 11 (nilai x sebelum decrement)
console.log(x); // Output: 10

```

### Penjelasan Postfix dan Prefix
1. **Prefix** (++a/--a): Variabel ditingkatkan atau dikurangi terlebih dahulu sebelum nilai variabel digunakan dalam pernyataan.
2. **Postfix** (a++/a--): Variabel digunakan dalam pernyataan terlebih dahulu sebelum ditingkatkan atau dikurangi.

### Contoh Kode

```js

let a = 3;
let b = 3;

console.log("Prefix increment:");
console.log(++a); // Output: 4 (nilai a ditingkatkan sebelum dicetak)
console.log(a);   // Output: 4

console.log("Prefix decrement:");
console.log(--b); // Output: 2 (nilai b dikurangi sebelum dicetak)
console.log(b);   // Output: 2

let x = 3;
let y = 3;

console.log("Postfix increment:");
console.log(x++); // Output: 3 (nilai x dicetak sebelum ditingkatkan)
console.log(x);   // Output: 4

console.log("Postfix decrement:");
console.log(y--); // Output: 3 (nilai y dicetak sebelum dikurangi)
console.log(y);   // Output: 2

```

## 9. Pengguna Loop Built-in Method di suatu Array
### Penjelasan
Javascript menyediakan loop built-in ___forEach___, ___map___, ___reduce___, ___filter___, dan ___find___ untuk mengulangi elemen dalam array.

### Contoh Kode
1. **forEach**: Menjalankan fungsi untuk setiap elemen dalam array, tidak mengembalikan apa pun.

```js

let numbers = [1, 2, 3, 4, 5];
numbers.forEach(function(number) {
    console.log(number);
});
// Output:
// 1
// 2
// 3
// 4
// 5

```
2. **map**: Membuat array baru dengan hasil dari fungsi yang diterapkan pada setiap elemen.

```js

let numbers = [1, 2, 3, 4, 5];
let doubled = numbers.map(function(number) {
    return number * 2;
});
console.log(doubled);
// Output: [2, 4, 6, 8, 10]

```
3. **reduce**: Menghasilkan satu nilai dari array dengan menjalankan fungsi yang diberikan pada setiap elemen. (___menghitung rata rata___)

```js

let numbers = [1, 2, 3, 4, 5];
let sum = numbers.reduce(function(total, number) {
    return total + number;
}, 0);
console.log(sum);
// Output: 15

```
4. **filter**: Membuat array baru dengan elemen yang lulus uji dari fungsi yang diberikan.

```js

let numbers = [1, 2, 3, 4, 5];
let evenNumbers = numbers.filter(function(number) {
    return number % 2 === 0;
});
console.log(evenNumbers);
// Output: [2, 4]

```
5. **find**: Mengembalikan nilai elemen pertama yang memenuhi fungsi uji yang diberikan atau ___undefined___ jika tidak ada elemen yang memenuhi kriteria.

```js

let numbers = [1, 2, 3, 4, 5];
let found = numbers.find(function(number) {
    return number > 3;
});
console.log(found);
// Output: 4

```

## 10. Cara Mengubah Suatu Tipe Data, Semisal String Menjadi Number
### Penjelasan:
Javascript menyediakan berbagai cara untuk mengonversi tipe data satu ke yang lain.

### Contoh Kode Konversi String > Number
___parseInt()___, ___parseFloat()___, ___Number()___, ___+___.

```js

let stringNumber = "10";
let number = parseInt(stringNumber);
console.log(number); // Output: 10

let floatString = "3.14";
let floatNumber = parseFloat(floatString);
console.log(floatNumber); // Output: 3.14

let str1 = "123";
let num1 = Number(str1);
console.log(num1); // Output: 123

let str1 = "123";
let num1 = +str1;
console.log(num1); // Output: 123

```

### Contoh Kode Konversi Number > String
___toString()___, ___String()___, ___template literals___, ___concatenation with empty string___.

```js

let number = 20;
let stringNumber = number.toString();
console.log(stringNumber); // Output: "20"

let booleanValue = true;
let stringBoolean = booleanValue.toString();
console.log(stringBoolean); // Output: "true"

let num = 123;
let str = String(num);
console.log(str); // Output: "123"

let num = 123;
let str = `${num}`;
console.log(str); // Output: "123"

let num = 123;
let str = num + '';
console.log(str); // Output: "123"

```

## 11. Konvensi & Rules Penulisan Nama Variables Di Javascript
### Penjelasan:
Javascript memiliki konvensi dan aturan penamaan variabel yang baik untuk memudahkan pembacaan dan pemahaman kode.

Rules:

1. only contains ___letter___ ___number___ ___&___ _
2. first character can't be number 
3. case sensitive
4. can't use reserved keywords: ___function___, ___let___, ___const___, ___var___, ___if___, ___else___, ___while___, ___for___, etc

### Contoh Kode Baik Dan Buruk

```js

// Baik
let firstName = "John";
let lastName = "Doe";
let age = 20;

// Buruk
let n = "John";
let LN = "Doe";
let a = 20;

```


## 12. Perbedaan Stack & Queue
### Penjelasan:
**Stack** dan **Queue** adalah struktur data linear yang digunakan untuk menyimpan dan mengelola data.

### Stack
1. Bekerja dengan prinsip LIFO (Last In, First Out).
2. Elemen yang terakhir ditambahkan adalah yang pertama kali dihapus.
3. Digunakan untuk operasi seperti undo/redo, navigasi browser, dan ekspresi matematika.

```js

class Stack {
  constructor() {
    this.data = [];
  }

  push(item) {
    this.data.push(item);
  }

  pop() {
    return this.data.pop();
  }

  peek() {
    return this.data[this.data.length - 1];
  }
}

let stack = new Stack();

stack.push("Hello");
stack.push("World");
stack.push("!");

console.log(stack.pop()); // Output: !
console.log(stack.peek()); // Output: World

```

### Queue
1. Bekerja dengan prinsip FIFO (First In, First Out).
2. Elemen yang pertama ditambahkan adalah yang pertama kali dihapus.
3. Digunakan untuk operasi seperti antrian antrian, buffering data, dan pemrosesan job.

```js

class Queue {
  constructor() {
    this.data = [];
  }

  enqueue(item) {
    this.data.push(item);
  }

  dequeue() {
    return this.data.shift();
  }

  front() {
    return this.data[0];
  }
}

let queue = new Queue();

queue.enqueue("John");
queue.enqueue("Doe");
queue.enqueue("20");

console.log(queue.dequeue()); // Output: John
console.log(queue.front()); // Output: Doe

```


## 16. Pahami Perbedaan antara block dan global scope serta konsekuensi dari Perbedaan scoped tersebut
### Penjelasan:
Scope mengacu pada lingkup di mana variabel dapat diakses dalam program.

### Jenis Scope:
1. **Block Scope**: Variabel hanya dapat diakses di dalam blok kode di mana mereka dideklarasikan.
2. **Global Scope**: Variabel dapat diakses dari mana saja dalam program.

### Contoh Kode

```js

// Block Scope
function greet() {
  let name = "John Doe";
  console.log(name); // Output: John Doe
}

console.log(name); // Error: name is not defined outside of the function

```

## 17. Cara menambah, mengurangi dan menyortir suatu array
### Penjelasan:
Javascript menyediakan method built-in untuk ___menambah___, ___mengurangi___, dan ___menyortir array___.

1. Menambah

```js

let numbers = [1, 2, 3];
numbers.push(4);
console.log(numbers); // Output: [1, 2, 3, 4]

```
2. Mengurangi

```js

let numbers = [1, 2, 3, 4];
numbers.pop();
console.log(numbers); // Output: [1, 2, 3]

```
1. Menyortir

```js

let numbers = [4, 2, 1, 3];
numbers.sort(); // Mengurutkan secara ascending
console.log(numbers); // Output: [1, 2, 3, 4]

```


## 18. Cara akses data di dalam suatu multi-dimension array
### Penjelasan:
Multi-dimensional array digunakan untuk menyimpan data dalam struktur yang lebih kompleks, seperti tabel.


### Contoh Kode

```js

let students = [
  ["John Doe", 20, "Software Engineer"],
  ["Jane Doe", 22, "Designer"],
  ["Peter Jones", 18, "Student"]
];

console.log(students[0][1]); // Output: 20 (akses umur John Doe)
console.log(students[2][0]); // Output: Peter Jones (akses nama Peter Jones)

```

___students[0][1]___ 

[0] mengakses sub-array pertama & [1] mengakses elemen kedua dari sub-array pertama


## 19. Logika aritmatika antara 2 tipe data yang berbeda beda di JavaScript
### Penjelasan:
Operator aritmatika dapat digunakan pada tipe data yang berbeda, tetapi hasilnya mungkin tidak selalu seperti yang diharapkan.

### Contoh Kode

```js

let number = 10;
let stringNumber = "20";

console.log(number + stringNumber); // Output: 30 (stringNumber dikonversi ke number)
console.log(stringNumber - number); // Output: 10 (number dikonversi ke string)

```


## 20. Perbedaan jenis jenis loop di JavaScript 
### Penjelasan
Javascript menyediakan berbagai jenis loop untuk mengulangi kode dalam blok tertentu.

### Jenis Loop & Contoh Kode
1. **for**: Mengulangi kode berdasarkan nilai counter.

```js

for (let i = 0; i < 5; i++) {
  console.log(i);
}

```
2. **while**: Mengulangi kode selama kondisi tertentu terpenuhi.

```js

let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}

```
3. **do-while**: Mengulangi kode minimal sekali, kemudian mengecek kondisi.

```js

let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);

```
4. **for...of**: Mengulangi elemen dalam array atau string.

```js

let numbers = [1, 2, 3, 4, 5];
for (let number of numbers) {
  console.log(number);
}

```
5. **for...in**: Mengulangi properti dalam object.

```js

let person = {
  name: "John Doe",
  **age: 20,
  occupation: "Software Engineer"
};

for (let property in person) {
  console.log(property);
}

```


## 21. Callback Basic
### Penjelasan:
Callback adalah fungsi yang dipass sebagai argumen ke fungsi lain. Fungsi callback dipanggil setelah fungsi utama selesai dijalankan.

### Contoh Kode

```js

function greet(name, callback) {
  console.log("Hello, " + name + "!");
  callback();
}

greet("John Doe", function() {
  console.log("Goodbye!");
});

```


## 22. Karakteristik Array
### Penjelasan:
Array di Javascript memiliki beberapa karakteristik penting:

1. **Heterogeneous**: Dapat menyimpan elemen dengan tipe data yang berbeda.
2. **Ordered**: Elemen di dalam array memiliki urutan.
3. **Dynamic**: Ukuran array dapat berubah secara dinamis.
4. **Zero-based**: Pengindeksan elemen array dimulai dari 0.


## 23. Logika perbandingan antara dua tipe data yang berbeda (1000 === undefined)
### Penjelasan:
Operator perbandingan di Javascript dapat digunakan untuk membandingkan nilai dengan tipe data yang berbeda.

### Contoh Kode

```js

let number = 10;
let stringNumber = "10";

console.log(number === stringNumber); // Output: false (nilai sama, tipe data berbeda)
console.log(number == stringNumber); // Output: true (nilai dikonversi ke tipe data yang sama)

```


## 24. Cara memanipulasi suatu string menggunakan array/string built-in method (concat/join/split/replace)
### Penjelasan:
Javascript menyediakan operator dan method untuk menentukan tipe data suatu nilai.

### Penjelasan & Contoh Kode
1. **concat**: digunakan untuk menggabungkan 2 atau lebih string.

```js

const namaDepan = "Rina";
const namaBelakang = "Wijaya";
const namaLengkap = namaDepan.concat(" ", namaBelakang);

console.log(namaLengkap); // Output: Rina Wijaya

```

2. **join**: digunakan untuk menggabungkan elemen-elemen array menjadi string, dengan menambahkan pemisah di antara elemen.

```js

const namaBuah = ["Apel", "Mangga", "Pisang"];
const buahGabungan = namaBuah.join(", ");

console.log(buahGabungan); // Output: Apel, Mangga, Pisang

```

3. **split**: digunakan untuk memisahkan string menjadi array berdasarkan pemisah yang ditentukan.

```js

const kalimat = "Saya suka belajar JavaScript";
const kataKata = kalimat.split(" ");

console.log(kataKata); // Output: ["Saya", "suka", "belajar", "JavaScript"]

```


4. **replace**: digunakan untuk mengganti karakter atau kata tertentu dalam string dengan karakter atau kata lain.


```js

const teks = "Halo, nama saya Rina";
const teksBaru = teks.replace("Rina", "Budi");

console.log(teksBaru); // Output: Halo, nama saya Budi

```


## 25. [Big-O Notation Guide](big-o-complexity.png)
1. Constant O(1) = tidak ada loop
2. Linear O(n) = ada 1 loop
3. Quadratic O(n^2) = ada loop di dalam loop
4. Logarithmic O(logn) = ada operasi secara logaritmik, **cth** ___mencari array yang diurutkan menggunakan pencarian biner___.