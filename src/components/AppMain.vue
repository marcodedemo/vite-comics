
<script>
  export default{
    data(){
      return{

      

      }
    },
    
  }

</script>

<template>
  <main>

    <div id="jumbotron"></div>


    <div id="container-centered">

      <div id="series">

        <div id="tag">
          <strong>Current Series</strong>
        </div>

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
        align-items: center;

        position: relative;
        
        height: 300px;
        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;

        padding: 0 20px;

      #series{


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
      }
        
      
    }
}
</style>