<template>
    <div>
        <h1 id="count">Count {{ count }}</h1>
        <p>Click the button to see the message</p>
        <button @click="count++">Add 1</button>
        <button @click="addCount">Click me</button>
        <!-- <p>{{ message }}</p> -->
    </div>
</template>
<script>
export default {
    data() {
        return {
            message: '',
            count: 0
        }
    },
    methods: {
        showMessage() {
            this.message = 'Hello World!'
        },
        addCount() {
            this.count++
        }
    },
    beforeCreate() {
     console.log('beforeCreate')
   },
   created() {
     console.log('created')
   },
   beforeMount() {
     console.log('beforeMount count: ' + this.count);
   },
   mounted() {
     console.log('mounted')
   }, 
   beforeUpdate() {
    //  console.log('State beforeUpdate count: ' + this.count);
     console.log('beforeUpdate ',document.getElementById('count').innerText);
   },
   updated() {
    //  console.log('State updated count: ' + this.count);
        console.log('updated ',document.getElementById('count').innerText);
   },
   beforeUnmount() {
     console.log('beforeUnmount')
   },
   unmounted() {
     console.log('unmounted')
   } 
}
</script>