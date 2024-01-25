<script >
  
  import AppHeader from './components/AppHeader.vue'
  
  

  export default {
  components:{  AppHeader }
  }
</script>

<template>

  <div class="container">
    <AppHeader />
    <router-view class="page"></router-view>
  </div>
 

  
</template>

<style lang="scss">
@use './assets/styles/general.scss' as *;

.container{
  
}

</style>
