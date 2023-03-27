
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
        ],

        dropdownShow: false,
      }
    },

    methods:{
      showDropdownContent(){
        this.dropdownShow = !this.dropdownShow;
      }
    }
    
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

        <div id="pc-menu">

          <ul id="links">
            <li v-for="link in links">
              <a href="#">{{ link }}</a>
            </li>
          </ul>
          
        </div>

        <div id="mobile-menu">

          <div id="hamburger-menu" @click="showDropdownContent()">

            <i class="fa-solid fa-bars"></i>
          
            <ul v-show="dropdownShow" id="dropdown-content">
              <li v-for="link in links">
                <a href="#">{{ link }}</a>
              </li>
            </ul>

          </div>
            
        </div>
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

    #pc-menu{
      // display: none;

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

    #mobile-menu{
      display: none;

      #hamburger-menu{
        position: relative;

        background-color: transparent;
        border: none;

        font-size: 2em;

        &:hover #dropdown-content{
          display: block;
        }

        #dropdown-content{

          background-color: white;
          position: absolute;
          top: 40px;
          right: -20px;

          z-index: 1;

          li{
            padding: 0 20px;

            text-transform: capitalize;

            &:hover{
              background-color: rgba(128, 128, 128, 0.282);
            }
          }



        }
      }


    }

  }
}


@media screen and (max-width: 992px) {

  #container-centered{
    
    #logo{
      flex-shrink: 0;
    }

    #pc-menu{
      display: none;
    }

  }
  
  header #container-centered #mobile-menu{
    display: block; 
  }
}
</style>