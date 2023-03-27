
<script>
  export default{
    data(){
      return{

        links:[
            {
                img: "/public/img/buy-comics-digital-comics.png",
                text:"digital comics",
            },
            {
                img: "/public/img/buy-comics-merchandise.png",
                text:"dc merchandise",
            },
            {
                img: "/public/img/buy-comics-subscriptions.png",
                text:"subscription",
            },
            {
                img: "/public/img/buy-comics-shop-locator.png",
                text:"comic shop locator",
            },
            {
                img: "/public/img/buy-dc-power-visa.svg",
                text:"dc power visa",
            },
        ]

      }
    },
    
  }

</script>

<template>
  <section>
    <div id="container-centered">

        <div class="card" v-for="(link, index) in links">

            <a href="#">

                <div class="logo">
                    <img :src="links[index].img" alt="">
                </div>
                
                <div class="text">
                    {{ link.text }}
                </div>
            </a>

        </div>


    </div>
  </section>
</template>

<style lang="scss" scoped>

section{
    background-color: #0582f9;

    #container-centered{
        display: flex;
        align-items: center;

        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;

        padding: 60px 20px;

        .card{

            width: calc(100% / 5);

            a{
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 10px;
                .logo{
                    width: 60px;
                    height: 60px;

                    flex-shrink: 0;
                    
                    img{
                        width: 100%;
                        height: 100%;
                        object-fit: contain;
                    }
                }
                
                .text{
                    text-transform: uppercase;
                    color: white;
                    font-size: .9em;
                }
            }
        }
    }
}


@media screen and (max-width: 992px){
    
    section #container-centered{
        flex-wrap: wrap;
        justify-content: center;
    }
    section #container-centered .card{
        width: calc(100% / 3);
        padding: 20px;
    }
}

@media screen and (max-width: 768px){

    section #container-centered{
        flex-direction: column;
        gap: 0;

        padding: 0;
    }
    section #container-centered .card{
        width: 100%;
    }
}
</style>