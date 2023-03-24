
<script>
  export default{
    data(){
      return{

        mainInnerText: "--> Content goes here <--"

      }
    },
    
  }

</script>

<template>
  <main>
    <div id="container-centered">

        <div id="inner-text">{{ mainInnerText }}</div>

    </div>
    </main>
</template>

<style lang="scss" scoped>

main{

    background-color: #1c1c1c;
    
    #container-centered{
        display: flex;
        align-items: center;
        
        height: 300px;
        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;
        
        #inner-text{
            color: white;
            font-weight: bold;
            font-size: 2em;
            
        }
    }
}
</style>