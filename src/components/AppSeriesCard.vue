

<script>

export default{
    data(){
        return{

        }
    },

    props:{
        img: String,
        title: String,

    }
}

</script>



<template>
    <div id="card">

        <div id="thumb">
            <img :src="img" alt="">
        </div>

        <span id="title">{{title}}</span>
        
    </div>
</template>



<style lang="scss" scoped>

#card{
    display: flex;
    flex-direction: column;
    gap: 15px;

    width: calc(100% / 6 - (20px * 5 / 6));

    #thumb{

        width: 100%;
        height: 200px;


        img{
            width: 100%;
            height: 100%;

            object-fit: cover;
        }
    }

    #title{
        color: white;
        text-transform: uppercase;
        font-weight: bold;
        font-size: .8em;
    }

}

@media screen and (max-width:768px) {
    
    #card{
        width: calc(100% / 4 - 20px * 3 / 4);
    }
  
}

@media screen and (max-width:576px) {
  
    #card{
        width: calc(100% / 3 - 20px * 2 / 3);
    }
  
}

</style>