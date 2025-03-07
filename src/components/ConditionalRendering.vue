<template>
    <div v-if='status===1'>Ini Tampil {{ status }}</div>
    <div v-else-if='status==2'>Ini Tampil {{ status }}</div>
    <div v-else>Tidak Ada Status</div>
    <button @click="showStatus">Toggle Status</button>
</template>
<script>
export default{
    data(){
        return{
            status: 2
        }
    },
    methods:{
        showStatus(){
            if(this.status === 1){
                this.status = 2;
            }else if(this.status === 2){
                this.status = 3;
            }else{
                this.status = 1;
            }
        }
    }
}</script>