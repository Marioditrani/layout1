
<script >

export default {
    data(){
    return{
      sideMenuValue: 0,
      infomenu: 0,
        
    }
  },
  methods: {
    openside() {
            if (this.sideMenuValue) {
                this.sideMenuValue = 0
            } else {
                this.sideMenuValue = 1

            }
            console.log(this.sideMenuValue)
        
        },
        infoside() {
            if (this.infomenu) {
                this.infomenu = 0
            } else {
                this.infomenu = 1
            }
        },
    
    },

  
  }
  
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
    <div class="nav-mb">
      <div class="btn-menu" @click="openside" >
        <div class="l2" :class="sideMenuValue? 'l1-on':''"></div>
        <div class="l2" :class="sideMenuValue? 'l2-on':''"></div>
        <div class="l2" :class="sideMenuValue? 'l3-on':''"></div>
      </div>
    </div>

    <div  :class="this.sideMenuValue? 'nav-mb-on': 'nav-mb-off'">
        <div :class="this.sideMenuValue? 'top-on': 'top-off'">
         <router-link :to="{ name: 'home' }" class="link" @click="openside">home</router-link>
         <router-link :to="{ name: 'prenotaServizio' }" class="link" @click="openside" >prenota tavolo</router-link>
         <router-link :to="{ name: 'prenota' }" class="link" @click="openside" >prenota asporto</router-link>
         <router-link :to="{ name: 'chi-siamo' }" class="link" @click="openside" >chi siamo</router-link>
         <router-link :to="{ name: 'Contatti' }" class="link" @click="openside" >contatti</router-link>
         <router-link :to="{ name: 'menu' }" class="link" @click="openside" >menu</router-link>
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
  z-index: 5!important;
  .left-header{
    display: flex;
    align-items: center;
    gap: 20%;
    .logo{
      width: 200px;
      aspect-ratio: 1;
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


.nav-mb{
    display: none;
    position: relative;
    width: 100%;   
  .btn-menu{
    position: fixed;
    right: 50px;
    top: 110px;
    flex-direction: column;
    gap: .7rem;
    align-items: flex-end;
    display: flex;
    z-index: 5!important;
    .l2{
      z-index: 10;
      width: 50px;
      height: 5px;
      border-radius: 20px;
      background-color: white;
     
    }
    
    
    }
    
    
  }

  .nav-mb-on{
    position: fixed;
    top: 0;
    left: 0;
    background-color: #270000;
    width: 100%;
    height: 100%;
    transition: all .3s linear;
   
  
    }

    .nav-mb-off{
    position: fixed;
    top: 0;
    left: 0;
    background-color: #270000;
    width: 100%;
    height: 0;
    transition: all .2s linear;

    

  }

  .l1-on{
    transform: rotateZ(-45deg);
  }
  .l2-on{
    position: fixed;
    transform: rotateZ(45deg);
  }
  .l3-on{
    display: none;
  }
  
  .top-off{
    display: none;
    
    
  }
  .top-on{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    padding: 10%;
    height: 100%;
    margin-top: 4rem;
    
    .link{
      color: white;
      font-size: 23px;
      z-index: 10!important;
      position: relative!important;
    }
  }

  

@media (max-width: 1700px) {
  
  .right-header{
    display: none!important;
  }
  .nav-mb{
    display: block!important;
    z-index: 2!important;
  }
  
 
}
@media (max-width: 700px) {
  
  header{
    padding: 5rem 2rem!important;
  }

}
@media (max-width: 600px) {
  
  header{
    .left-header{
      .logo{
        width: 150px;
      }
      .title{
        display: none;
      }
    }
  }

}
</style>
