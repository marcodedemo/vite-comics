

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

        <img :src="img" alt="">
        <span id="title">{{title}}</span>
        
    </div>
</template>



<style lang="scss" scoped>

#card{
    display: flex;
    flex-direction: column;
    gap: 15px;

    width: calc(100% / 6 - (20px * 5 / 6));

    img{
        width: 100%;
    }

    #title{
        color: white;
        text-transform: uppercase;
        font-weight: bold;
        font-size: .8em;
    }

}


</style>