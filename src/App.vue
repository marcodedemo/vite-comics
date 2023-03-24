

<script>

  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppLinkSection from './components/AppLinkSection.vue';
  import AppFooter from './components/AppFooter.vue';


  export default{
    data(){
      return{

      }
    },

    components: {
      AppHeader,
      AppMain,
      AppLinkSection,
      AppFooter,

      
    }

  }

</script>

<template>
  <div>

    <AppHeader></AppHeader>
    <AppMain></AppMain>
    <AppLinkSection></AppLinkSection>
    <AppFooter></AppFooter>
    

  </div>
</template>

<style lang="scss" scoped>


</style>