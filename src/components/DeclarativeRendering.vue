<template>
    <div>{{ message }}</div>
    <span :title='message'>Ini Span</span>
</template>
<script>
 export default{
     data(){
         return{
             message: 'Hello Vue!'
         }
     }
 }
</script>