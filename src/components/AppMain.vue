
<script>

  import AppSeriesCard from './AppSeriesCard.vue';

  export default{
    data(){
      return{

        comics:[
          {
            "thumb": "https://picsum.photos/200",
            "price": "$19.99",
            "series": "Action Comics",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$3.99",
            "series": "American Vampire 1976",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$16.99",
            "series": "Aquaman",
            "type": "graphic novel"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$2.99",
            "series": "Batgirl",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$3.99",
            "series": "Batman",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$2.99",
            "series": "Batman Beyond",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$3.99",
            "series": "Batman/Superman",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$4.99",
            "series": "Batman/Superman Annual",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$5.99",
            "series": "Batman: The Joker War Zone",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$6.99",
            "series": "Batman: Three Jokers",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$4.99",
            "series": "Batman: White Knight Presents: Harley Quinn",
            "type": "comic book"
          },
          {
            "thumb": "https://picsum.photos/200",
            "price": "$16.99",
            "series": "Catwoman",
            "type": "graphic novel"
          }
        ]

      

      }
    },

    components:{
      AppSeriesCard,
    }
    
  }

</script>

<template>
  <main>

    <div id="jumbotron"></div>


    <div id="container-centered">

      <div id="tag">
        <strong>Current Series</strong>
      </div>

      <div id="series">

        <AppSeriesCard v-for="comic in comics" :title="comic.series" :img="comic.thumb"></AppSeriesCard>
        
      </div>
      
      <div id="load-more">
        <button>Load More</button>
      </div>
      
    </div>
    

    </main>
</template>

<style lang="scss" scoped>

main{


  background-color: #1c1c1c;

    

    #jumbotron{
        width: 100%;
        height: 400px;

        background-image: url("/public/img/jumbotron.jpg");
        background-repeat: no-repeat;
        background-size: cover;
    }

    #container-centered{
        display: flex;
        flex-direction: column;

        position: relative;
        
        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;

        padding: 40px 20px;



        #tag{
          position: absolute;
          top: 0;
          left: 0;

          transform: translateY(-50%);

          background-color: #0582f9;
          color: white;

          font-size: 1.6em;

          text-align: center;
          white-space: nowrap;
          text-transform: uppercase;

          padding: 4px 16px;
          
        }



        #series{
          display: flex;
          flex-wrap: wrap;

          gap: 20px;


        }
        
      
        #load-more {
    
        text-align: center;

        margin: 30px 0;
    
        & button{
          
          color: white;
          background-color: #0582f9;
          
          border: none;
          
          text-transform: uppercase;
          font-weight: bold;
          
          padding: 10px 30px;
          
          
        }
      }
    }

}
</style>