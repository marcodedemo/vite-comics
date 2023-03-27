

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



<style>

#card{
    display: flex;
    flex-direction: column;

    align-items: center;

}


</style>