
<script >
  
  export default {
    data(){
    return{
        obs:1,
            carouselMain:[
                {
                    
                },
                {
                    img : "../assets/img/bigimage.png",
                    paragrafo : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "PRENOTA",
                    titolo : "Titolo paragrafo1",
                },
                {
                    img : "",
                    paragrafo : "ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "MENU",
                    titolo : "Titolo paragrafo2",
                },
                {
                    img : "",
                    paragrafo : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "ooooooo",
                    titolo : "Titolo paragrafo3",
                }
            ]
    }
  },
  methods: {
    imgright(){
        if(this.obs == 3){
            this.obs = 1
        }else{
            this.obs ++
        } 
       
    },
    imgleft(){
        if(this.obs == 1){
            this.obs = 3
            
        }else{
            this.obs --
            
        }
            
     }
    },

  
  }
</script>


<template>

<main>
    <div class="left-main" :class="this.obs == 1 ? 'img1': '',this.obs == 2 ? 'img2' : '',this.obs == 3 ? 'img3' : ''">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat nobis rerum autem eligendi facilis officiis mollitia fugit, voluptates numquam iusto. Sint maxime natus voluptatibus, quisquam ipsum corporis? Aliquam, ea nisi.</p>
        <div class="right-main-mb">
            <h2>{{ this.carouselMain[obs].titolo }}</h2>
            <p>{{ this.carouselMain[obs].paragrafo }}</p>
            <span class="button">{{ this.carouselMain[obs].link }}</span>
        </div>
        <div class="button-carousel">
            <div class="left-arrow">
                <svg xmlns="http://www.w3.org/2000/svg" width="30px" height="30px" fill="currentColor" class="bi bi-arrow-left" viewBox="0 0 16 16" @click="imgleft">
                    <path fill-rule="evenodd" d="M15 8a.5.5 0 0 0-.5-.5H2.707l3.147-3.146a.5.5 0 1 0-.708-.708l-4 4a.5.5 0 0 0 0 .708l4 4a.5.5 0 0 0 .708-.708L2.707 8.5H14.5A.5.5 0 0 0 15 8"/>
                </svg>
            </div>
            <div class="number">
                <div class="active-image"><span>{{ this.obs }} / 3</span></div>
            </div>
            <div class="right-arrow">
                <svg xmlns="http://www.w3.org/2000/svg" width="30px" height="30px" fill="currentColor" class="bi bi-arrow-right" viewBox="0 0 16 16" @click="imgright">
                    <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8"/>
                </svg>
            </div>
        </div>
        
    </div>
    <div class="right-main">
        <div class="top-right">
            <h2>{{ carouselMain[obs].titolo }}</h2>
            <p>{{ carouselMain[obs].paragrafo }}</p>
            <span class="button">{{ carouselMain[obs].link }}</span>
        </div>
        <div class="bottom-right">
            <div class="left-bottom">
                <h3>orari d'apertura</h3>
                <div class="container-og">
                    <div class="container-giorni">
                        <span>lunedi</span>
                        <span>martedi</span>
                        <span>mercoledi</span>
                        <span>giovedi</span>
                        <span>venerdi</span>
                        <span>sabato</span>
                        <span>domenica</span>
                    </div>
                    <div class="container-orari">
                        <span>chiuso</span>
                        <span>16-22</span>
                        <span>16-22</span>
                        <span>16-22</span>
                        <span>16-22</span>
                        <span>16-22</span>
                        <span>16-22</span>
                    </div>
                </div>
            </div>
            <div class="right-bottom">
                <h3>dove trovarci</h3>
                <h4>Via lorem ipsum 12, 34900 Citta</h4>
                <img src="../assets/img/maps.png" alt="">
            </div>
        </div>
    </div>

    
</main>
  
</template>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;



.img1{
    background: url('../assets/img/bigimage.png');
}
.img2{
    background: url('https://ilfattoalimentare.it/wp-content/uploads/2022/12/Depositphotos_505971914_L-1.jpg');
}
.img3{
    background: url(../assets/img/bigimage.png);
}
main{
    display: flex;
    width: 100%;
    height: 100%;
    align-items: stretch;
    overflow: hidden;
    .left-main{
        background-color: red;
        background-repeat: no-repeat;
        background-size: cover;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        flex-grow: 2;
        flex-shrink: 1;
        height: 100%;

            p{
                background-color: #4D0404;
                padding: 1rem;
                margin: 3rem 5rem;
                border-radius: 20px;
            }

            .button-carousel{
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 2rem;
                font-size: 30px;
                background-color: rgba(0, 0, 0, 0.719);
                margin-bottom: 4rem;
                padding: 1rem;

                svg{
                    display: flex;
                    justify-content: center;
                }

                .number{
                    display: flex;
                    gap: .8rem;
                }
            }

    }
    
    .right-main{
        background-color: #EBD59B;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        flex-grow: 1;
        flex-shrink: 2;
        overflow: auto;
        .top-right{
            padding: 5rem 3rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            h2{
                color: black;
                font-size: 27px;
                text-transform: uppercase;
            }
            p{
                color: black;
                font-size: 25px;
                padding-top: 2rem;
            }
            .button{
                background-color: #4D0404;
                padding: 1rem 2rem;
                margin-top: 2rem;
            }
        }
        .bottom-right{
            background-color: #4D0404;
            display: flex;
            justify-content: space-between;
            padding: 1rem;
            
            .left-bottom{
                width: 50%;
                h3{
                    padding: .5rem;
                    font-size: 22px;
                    text-transform: uppercase;
                }
                
                .container-og{
                    display: flex;
                    justify-content: space-between;
                    padding: 1rem;
                    .container-giorni, .container-orari{
                        display: flex;
                        flex-direction: column;
                        font-size: 20px;
                    }
                }
                
            }
            .right-bottom{
                display: flex;
                flex-direction: column;
                align-items: center;
                gap: 1rem;
                h3{
                    text-align: center;
                    padding: .5rem;
                    font-size: 22px;
                    text-transform: uppercase;
                }
                h4{
                    text-align: center;
                }
                img{
                    width: 200px;
                    
                }
            }
        }
    }
}

.right-main-mb{
    display: none!important;
}



@media (max-width: 900px) {

    .right-main{
        display: none!important;
    }
    .left-main{
        width: 100%!important;
    }
    .right-main-mb{
    display: block!important;
}

    
}
</style>
