
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
            <div class="logo">
                <img :src="links[index].img" alt="">
            </div>

            <div class="text">
                {{ link.text }}
            </div>
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

        padding: 60px;

        .card{
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;

            width: calc(100% / 5);

            .logo{
                width: 60px;
                height: 60px;

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
</style>