<template>
     <h1>Hasil penjumlhan {{hasil}}</h1>
    <input type="text" v-model="angka1" />
    <input type="text" v-model="angka2" />
</template>
<script>

export default{
   data(){
       return{
           angka1: 0,
           angka2: 0
       }
   },
   computed:{
       hasil(){
           return parseInt(this.angka1) + parseInt(this.angka2)
       }
   }
}
</script>
