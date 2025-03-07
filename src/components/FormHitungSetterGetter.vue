<template>
     <h1>{{ title }} {{hasil}}</h1>
     <h1>{{ discount }}</h1>
    <input type="text" v-model="angka1" />
    <input type="text" v-model="angka2" />
    <button @click="addDiscount">+ Discount</button>
</template>
<script>

export default{
   data(){
       return{
           title:"Form Hitung ",
           angka1: 0,
           angka2: 0
       }
   },
   computed:{
      discount:{
        get(){
            return parseInt(this.angka1) + parseInt(this.angka2);
        },
        set(value){
            this.angka1 -= value;
            this.angka2 -= value;
        }
      }
   },
   methods:{
    addDiscount(){
        this.discount = 500;
    }
   }
}
</script>
