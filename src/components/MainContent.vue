<script>
import CardsContent from  '../components/CardsContent.vue';
   export default{
    name:'MainContent',
    components:{
      CardsContent,
    },
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
            ],
            fumetti:[
                    {
                        "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                        "price": "$19.99",
                        "series": "Action Comics",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                        "price": "$3.99",
                        "series": "American Vampire 1976",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                        "price": "$16.99",
                        "series": "Aquaman",
                        "type": "graphic novel",
                    },
                    {
                        "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                        "price": "$2.99",
                        "series": "Batgirl",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                        "price": "$3.99",
                        "series": "Batman",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                        "price": "$2.99",
                        "series": "Batman Beyond",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                        "price": "$3.99",
                        "series": "Batman/Superman",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                        "price": "$4.99",
                        "series": "Batman/Superman Annual",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                        "price": "$5.99",
                        "series": "Batman: The Joker War Zone",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                        "price": "$6.99",
                        "series": "Batman: Three Jokers",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                        "price": "$4.99",
                        "series": "Batman: White Knight Presents: Harley Quinn",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                        "price": "$16.99",
                        "series": "Catwoman",
                        "type": "graphic novel",
                    },

                ]

         }
      }

   }
</script>

<template>
   <main>
      <div id="jumbo">

      </div>
      <div id="content">
         <span>current series</span>
         <div class="cards">
            <CardsContent v-for="(element, index) in fumetti"
            :key="index"
            :propsThumb="element.thumb"
            :propsSeries="element.series">
            
            </CardsContent>
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
   #jumbo{
      min-height: 300px;
      background-image: url(../assets/img/jumbotron.jpg);
      background-repeat: no-repeat;
      background-size: cover;
      background-position: top;
   }
   #content{
      padding: 30px;
      background-color: $bg-black ;
      position: relative;
      span{
            font-size: 24px;
            color: white;
            position: absolute;
            top: -30px;
            background-color: $bg-blu;
            padding: 10px;
            left: 10%;
            text-transform: uppercase;
         }
      div{
         width: 80%;
         margin: 0 auto;
        
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
   .cards{
      width: 80%;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      gap: 20px;

   }
   
</style>