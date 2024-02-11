<script>
   export default{
    name:'FooterContent',
      data(){
         return{
            comicsLink:[
               {
                  link:'#',
                  testo:'characters',
               },
               {
                  link:'#',
                  testo:'comics',
               },
               {
                  link:'#',
                  testo:'movies',
               },
               {
                  link:'#',
                  testo:'tv',
               },
               {
                  link:'#',
                  testo:'games',
               },
               {
                  link:'#',
                  testo:'videos',
               },
               {
                  link:'#',
                  testo:'news',
               },
            ],
            shopLink:[
               {
                  link:'#',
                  testo:'shop dc'
               },
               {
                  link:'#',
                  testo:'shop dc collectibles'
               },
            ],
            dcLink:[
               {
                  link:'#',
                  testo:'terms of use',
               },
               {
                  link:'#',
                  testo:'privacy policy (new)',
               },
               {
                  link:'#',
                  testo:'ad choice',
               },
               {
                  link:'#',
                  testo:'advertising',
               },
               {
                  link:'#',
                  testo:'job',
               },
               {
                  link:'#',
                  testo:'subscriptions',
               },
               {
                  link:'#',
                  testo:'talent workshop',
               },
               {
                  link:'#',
                  testo:'cpsc certificates',
               },
               {
                  link:'#',
                  testo:'rating',
               },
               {
                  link:'#',
                  testo:'shop help',
               },
               {
                  link:'#',
                  testo:'contact us',
               },
            ],
            sitesLink:[
               {
                  link:'#',
                  testo:'dc',
               },
               {
                  link:'#',
                  testo:'mad magazine',
               },
               {
                  link:'#',
                  testo:'dc kids',
               },
               {
                  link:'#',
                  testo:'dc universe',
               },
               {
                  link:'#',
                  testo:'dc power visa',
               },
            ]
         }
      },
      methods:{
         capitalize(parole){
            parole=parole.split(' ');
            for (let i=0; i<parole.length; i++){
               parole[i] = parole[i].charAt(0).toUpperCase() + parole[i].slice(1);
            }
            return parole.join(' ');
         }
      }

   }
</script>

<template>
   <footer>
      <div id="top">
         <div class="container">
            <div id="links">
               <div>
                  <h4>dc comics</h4>
                  <ul>
                     <li v-for="(element, index) in comicsLink" :key="index">
                        <a :href="element.link">{{ capitalize(element.testo) }}</a>
                     </li>
                  </ul>
                  <ul>
                     <h4>shop</h4>
                     <li v-for="(element, index) in shopLink" :key="index">
                        <a :href="element.link">{{ capitalize(element.testo) }}</a>
                     </li>
                  </ul>
               </div>
               <div>
                  <h4>dc</h4>
                  <ul>
                     <li v-for="(element, index) in dcLink" :key="index">
                        <a :href="element.link">{{ capitalize(element.testo) }}</a>
                     </li>
                  </ul>
               </div>
               <div>
                  <h4>sites</h4>
                  <ul>
                     <li v-for="(element, index) in sitesLink" :key="index">
                        <a :href="element.link">{{capitalize(element.testo) }}</a>
                     </li>
                  </ul>
               </div>

            </div>
            <div id="logo">
               
            </div>
         </div>
      </div>
      <div id="bottom" >
         <div class="container">
            <div id="signUp">
               <button>sign-up</button>
            </div>
            <div id="icons">
               <h3>follow us</h3>
               <figure><img src="../assets/img/footer-facebook.png" alt=""></figure>
               <figure><img src="../assets/img/footer-twitter.png" alt=""></figure>
               <figure><img src="../assets/img/footer-youtube.png" alt=""></figure>
               <figure><img src="../assets/img/footer-periscope.png" alt=""></figure>
               <figure><img src="../assets/img/footer-pinterest.png" alt=""></figure>
            </div>

         </div>
      </div>
      

   </footer>
</template>

<style lang="scss" scoped>

@use '../scss/partials/mixins.scss' as *;
@use '../scss/partials/variables.scss' as*;

   #top{
      background-image: url('../assets/img/footer-bg.jpg');
      background-repeat: no-repeat;
      background-size: cover;
      .container{
         width: 80%;
         margin: 0 auto;
         display: flex;
         div{
            @include d-flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: flex-start;
         }
         #links{
            display: flex;
            flex-direction: row;
            width: 50%;
            margin-top: 20px;
            gap: 20px;

         }

      }
   }
   h4{
      text-transform: uppercase;
      color: white;
      margin-bottom: 10px;
   }
   h3{
      align-self: center;
      color: $bg-blu;
      text-transform: uppercase;
   }
   a{
      color: $grigio;
   }
   ul{
      @include d-flex;
      flex-direction: column;
      gap: 5px;
      align-items: flex-start;
      margin-bottom: 10px; 
   }
   #logo{
      width: 50%;
      background-image: url('../assets/img/dc-logo-bg.png');
      background-repeat: no-repeat;
      background-size: 90%;
      background-position: center;
   }
 
   #bottom{
      background-color: $bg-grigio;
      .container{
         display: flex;
         justify-content: space-between;
         padding: 30px;
         width: 80%;
         margin: 0 auto;
      }
      #signUp{
         
         button{
            border: 2px  solid $bg-blu;
            padding: 10px;
            text-transform: uppercase;
            color: white;
            background-color: $bg-grigio;
         }
      }
      #icons{
         display: flex;
         gap: 20px;
      }
   }

</style>