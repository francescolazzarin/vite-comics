<script>
   export default{
    name:'AppMain',
      data(){
         return{
            linkMain:[
               {
                  url:'./src/assets/img/buy-comics-digital-comics.png',
                  testo:'digital comics',
               },
               {
                  url:'./src/assets/img/buy-comics-merchandise.png',
                  testo:'dc merchandise'
               },
               {
                  url:'./src/assets/img/buy-comics-subscriptions.png',
                  testo:'subscription',
               },
               {
                  url:'./src/assets/img/buy-comics-shop-locator.png',
                  testo:'comic shop locator',
               },
               {
                  url:'./src/assets/img/buy-dc-power-visa.svg',
                  testo:'dc power visa',
               },
            ]
         }
      }

   }
</script>

<template>
   <main>
      <div id="content">
         <div>
            <span>--content goes here-- </span>
         </div>
      </div>
      <div id="link">
         <div class="container">
            <figure v-for="(element, index) in linkMain"  :key="index">
               <img :src="element.url" alt="">
               <a href="">{{ element.testo.toUpperCase() }}</a>
            </figure>
         </div>
      </div>
   </main>
</template>

<style lang="scss" scoped>
   @use '../scss/partials/variables.scss' as *;
   @use '../scss/partials/mixins.scss' as*;
   #content{
      padding: 30px;
      background-color: $bg-black ;
      div{
         width: 80%;
         margin: 0 auto;
         span{
            font-size: 24px;
            color: white;
         }
      }
   }
   #link{
      background-color: $bg-blu;
      padding: 40px;
      .container{
         width: 80%;
         margin: 0 auto;
         @include d-flex;
         gap:30px;
         figure{
            @include d-flex;
            gap: 10px;
            img{
               height: 50px;
            }
            a{
               color: white;
            }
         }
      }
   }
   
</style>