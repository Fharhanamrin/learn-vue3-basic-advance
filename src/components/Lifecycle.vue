<template>
  <div>Ini adalah parent component</div>
   <child-component text="hello world"></child-component>
   <child-component
    v-for="todo in todos"
    :key="todo" 
    :text="todo"></child-component>
</template>

<script>
 import ChildComponent from './components/ChildComponent.vue';

 export default {
   components: {
     ChildComponent
   },
   data() {
     return {
       text: 'Dari Nilai Data',
       text1: 'Dari Nilai Data 1',
       text2: 'Dari Nilai Data 2',
       todos: ['pertama', 'kedua', 'ketiga'],
     }
   },
   beforeCreate() {
     console.log('beforeCreate')
   },
   created() {
     console.log('created')
   },
   beforeMount() {
     console.log('beforeMount')
   },
   mounted() {
     console.log('mounted')
   }, 
   beforeUpdate() {
     console.log('beforeUpdate')
   },
   updated() {
     console.log('updated')
   },
   beforeUnmount() {
     console.log('beforeUnmount')
   },
   unmounted() {
     console.log('unmounted')
   }  
 }


</script>
