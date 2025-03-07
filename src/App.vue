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
<script>
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
</script>
