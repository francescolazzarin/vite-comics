<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/MainContent.vue';
import AppFooter from './components/FooterContent.vue';


   export default{
    components:{
      AppHeader ,
      AppMain,
      AppFooter,
    }
   
   }
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppFooter/>
</template>

<style lang="scss">
  @use './scss/style.scss' as *;
</style>
