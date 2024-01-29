<script >
  
  import AppHeader from './components/AppHeader.vue'
  
  

  export default {
  components:{  AppHeader }
  }
</script>

<template>

  <div class="container">
    <AppHeader class="header"/>
    <router-view class="page"></router-view>
  </div>
 

  
</template>

<style lang="scss">
@use './assets/styles/general.scss' as *;

.container{
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100vh;
  overflow: hidden;


  
  .page{
    //overflow: auto;
    
  }
}

@media (max-width : 900px) {

  .header{
   display: none !important;;
  }
  
}

</style>
