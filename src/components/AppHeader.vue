
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
         <span>home</span>
         <span>prenota tavolo</span>
         <span>prenota asporto</span>
         <span>chi siamo?</span>
         <span>contatti</span>
         <span>menu</span>
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
    gap: 10rem;
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
      gap: 5rem;
      background-color: #A6252D;
      padding: 2rem;
      font-size: 20px;
    }
  }
}


</style>
