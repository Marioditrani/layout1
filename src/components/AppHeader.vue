
<script >
  
</script>


<template>
  <header>
    <div class="left-header">
      <div class="logo">
      </div>
      <div class="title">
        <span>nome locale </span>
      </div>
    </div>
    <div class="right-header">
      <div class="nav">
         <router-link :to="{ name: 'home' }" >home</router-link>
         <router-link :to="{ name: 'prenotaServizio' }"  >prenota tavolo</router-link>
         <router-link :to="{ name: 'prenota' }"  >prenota asporto</router-link>
         <router-link :to="{ name: 'chi-siamo' }"  >chi siamo</router-link>
         <router-link :to="{ name: 'Contatti' }"  >contatti</router-link>
         <router-link :to="{ name: 'menu' }"  >menu</router-link>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;

header{
  background-color: #781C1C;
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding: 5rem;
  text-transform: uppercase;
  .left-header{
    display: flex;
    align-items: center;
    gap: 20%;
    .logo{
      width: 100px;
      height: 100px;
      background-color: red;
    }
    .title{
      font-size: 30px;
    }

  }
  .right-header{
    display: flex;
    align-items: center;
    .nav{
      display: flex;
      flex-wrap: wrap;
      gap: 5rem;
      background-color: #A6252D;
      padding: 2rem;
      font-size: 20px;
    }
  }
}


</style>
