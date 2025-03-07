<template>
    <div>{{index}}-{{text}}</div>
</template>

<script>


export default {
    props:{
        text:{
            type: String,
            default: ''
        },
        index:{
            type: String,
            default: ''
        }
    }
}
</script>
