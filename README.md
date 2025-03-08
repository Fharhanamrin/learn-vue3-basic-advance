

# Hi, I'm Fharhan Amrin Sitanggang 👋

## Contact

Feel free to reach out if you have any questions or just want to chat!

- **Email:** fharhanamrin028@gmail.com
- **LinkedIn:** [Fharhan Amrin]
 *https://www.linkedin.com/in/fharhan-amrin-b68a06143/*
- **YouTube:** [Tempat Belajar Bersama]
  *https://www.youtube.com/@tempatbelajarbersama*

Thank you for visiting my GitHub profile!

# Vue 3 + Vite

# Learn vue3 basic to advance

## Documentation language indonesia & inggris




#### 1. Instalasi  Vuejs + Vite(web dev build tool)


```md
 npm init vite-app <project-name> 
 cd <project-name>
 npm install
 npm run dev
```
if you using Yarn : 

```md
 yarn create vite-app <project-name>
 cd <project-name>
 yarn 
 yarn dev
```

#### 2. Declarative Rendering 
  
```md
<template>
   <div>{{message}}</div>
   <span :title='Ini Title'></span>
</template>
<script>
export default {
  data(){
    return{
      message: 'Hello Vue 3',
      title:'Ini Title Vue3'
    }
  }
}
</script>
```
Tag `<template></template>`

Ini adalah tempat di mana Anda mendefinisikan struktur HTML dari komponen Vue. Semua elemen di dalam tag ini akan dirender ke dalam DOM ketika komponen diinstansiasi.

Print Nilai {{ message }}
{{message}}: Ini adalah cara untuk menampilkan data dari komponen ke dalam HTML. Dalam hal ini, nilai dari variabel message yang didefinisikan dalam bagian data() akan ditampilkan di dalam elemen <div>. Ketika nilai message berubah, tampilan akan otomatis diperbarui untuk mencerminkan perubahan tersebut.

```
Declarative Rendering
Declarative Rendering: Menyatakan apa yang ingin ditampilkan, 
dan framework menangani detailnya.
Contoh: menggunakan v-for di Vue.js.


Imperative Rendering
Imperative Rendering: Menjelaskan bagaimana cara 
menampilkan elemen, dengan langkah-langkah yang lebih rinci.
Contoh: menggunakan loop for di JavaScript.

Direktif
Direktif dalam konteks pemrograman, 
khususnya dalam framework seperti Vue.js, 
merujuk pada atribut khusus yang digunakan untuk 
memberikan instruksi kepada framework tentang bagaimana
elemen DOM harus diperlakukan atau bagaimana data harus diikat.

data
data(): Fungsi ini mengembalikan objek yang berisi
data reaktif untuk komponen. Dalam hal ini, 
kita memiliki properti count yang diinisialisasi dengan nilai 0

methods
methods: Objek ini berisi metode yang dapat
dipanggil dalam komponen. Metode greet akan meningkatkan
nilai count setiap kali dipanggil.


Data reaktif di Vue.js merujuk pada kemampuan
framework untuk secara otomatis memperbarui 
tampilan (UI) ketika data yang mendasarinya berubah.


```


Binding Attribute:
Binding Attribute menggunakan cara singkat :title, yang merupakan kepanjangan dari direktif v-bind dalam Vue.js. Ini digunakan untuk mengikat data dari komponen Vue.js ke atribut HTML, sehingga nilai atribut dapat bersifat dinamis berdasarkan data yang didefinisikan dalam Option API.

Kesimpulan
:title: Merupakan cara singkat untuk menulis v-bind:title.
v-bind: Digunakan untuk mengikat data dari komponen ke atribut HTML.
Atribut Dinamis: Nilai yang kita tulis, seperti :title, akan otomatis menjadi atribut HTML dan dapat berubah sesuai dengan data yang ada di dalam komponen.


contoh di atas adalah deklarative code pada vuejs3 menampilkan variabel
dari option api ke element vuejs kita
:title dan mencetak message di bagian div kita {{ message }}



#### 3. Methods/actions

Methods atau actions digunakan untuk melakukan aksi tertentu dalam komponen Vue.js. Contohnya, kita dapat menggunakan direktif @click untuk memanggil metode yang didefinisikan dalam properti Vue.js. Dalam contoh berikut, kita akan menggunakan metode bernama greet untuk meningkatkan nilai dari data global count setiap kali tombol diklik.



```
<template>
  <button @click="greet">Click me {{ count }}</button>
</template>
<script>
export default {
  data(){
    return{
     count:0
    }
  },
  methods:{
    greet(){
      this.count++
    }
  }
}
</script>
```


### 4. v-model 

```
v-model adalah salah satu direktif yang 
sangat penting dalam Vue.js yang digunakan untuk mengikat 
data antara elemen input dan data dalam komponen.
Ini memungkinkan Anda untuk membuat interaksi 
dua arah antara model data dan tampilan, 
sehingga setiap perubahan pada input akan
secara otomatis memperbarui data, dan sebaliknya.
```
2 way data binding 

v-model menerapkan konsep 2-way data binding, yang berarti bahwa perubahan pada elemen input akan langsung mempengaruhi data di dalam komponen, dan perubahan pada data juga akan memperbarui tampilan input.

kita menerapkan 2 directive vue.js  singkatnya v-model panjangnya :value @input="message = $event.target.value"


```
<template>
  <div>{{ message }}</div>
  <input v-model="message">
  <input :value="message" @input="message = $event.target.value">
</template>
<script>
export default {
  data(){
    return{
     message:'Hello Vue 3'
    }
  },
}
</script>
```


### 5. conditional rendering

Penjelasan :
Conditional rendering dalam Vue.js mirip dengan penggunaan pernyataan if dalam JavaScript. Ini memungkinkan Anda untuk menampilkan atau menyembunyikan elemen dalam template berdasarkan kondisi tertentu.

variabel global

```data(){
    return{
     isVisible: false,
     isLoading: false
    }
  }
```

 namun if else elseif kita di komponen vuenya

versi javascript



```
let isVisible = false;
let isLoading = false;
if (isVisible) {
   cetak konten
} else if (isLoading) {
   cetak loading
} else {
   cetak konten tersembunyi
}

```

```
<template>
  <div v-if="isVisible">
    <h1>Hello Vue 3</h1>
  </div>
  <div v-else-if="isLoading">
    <h1>Loading...</h1>
  </div>
  <div v-else>
    <h1>Content is hidden</h1>
  </div>
  <button @click="toggleVisibility">Toggle Visibility</button>
</template>

export default {
  data(){
    return{
     isVisible: false,
     isLoading: false
    }
  },
  methods:{
    toggleVisibility(){
      this.isLoading = true;
      setTimeout(() => {
        this.isLoading = false;
        this.isVisible = !this.isVisible;
      }, 1000);
    }
  }
}
```








  





