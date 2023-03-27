
/* --------------------------------- script --------------------------------- */
<script>
  export default{
    data(){
      return{

        links:[
          "charaters",
          "comics",
          "movies",
          "tv",
          "games",
          "collectibles",
          "videos",
          "fans",
          "news",
          "shop",
        ]
      }
    },
    
  }

</script>

/* -------------------------------- template -------------------------------- */
<template>

  
  <header>
    <div id="container-centered">
    
      <!-- header logo -->
      <div id="logo">
        <img src="/public/img/dc-logo.png" alt="DC logo">
      </div>
      
      <!-- navbar links -->
      <navbar>
        <ul id="links">
          <li v-for="link in links">
            <a href="#">{{ link }}</a>
          </li>
        </ul>
      </navbar>
      
      
    </div>
  </header>
</template>

/* ---------------------------------- style --------------------------------- */
<style lang="scss" scoped>

header{
  
  #container-centered{
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-between;
  align-items: center;

  height: 150px;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;

  padding: 0 20px;



  #logo{
    width: 80px;

    img{
      width: 100%;
    }
  }

  #links{
    display: flex;
    flex-flow: row nowrap;
    

    li{
      position: relative;
      text-transform: uppercase;
      font-weight: bold;
      font-size: .9em;

      padding: 0 12px;

      &:hover{
        color:#0582f9;
        // border-bottom: 4px solid #0582f9;
      }

      &:hover::after{
        content: "";
        background-color: #0582f9;
        height: 4px;
        width: 100%;

        position: absolute;
        bottom: calc(-150px / 2 + .9em - 2px);
        left: 50%;
        transform: translate(-50%);

      }
      
    }
  }
  }

}
</style>