<script>
   export default{
    name:'AppHeader',
    data(){
      return{
         linkHeader:[
            {
               testo:'characters',
               link:'#',
               linkCorrente:false,
            },
            {
               testo:'comics',
               link:'#',
               linkCorrente:true,
            },
            {
               testo:'movies',
               link:'#',
               linkCorrente:false,
            },
            {
               testo:'tv',
               link:'#',
               linkCorrente:false,
            },
            {
               testo:'games',
               link:'#',
               linkCorrente:false,
            },
            {
               testo:'collectibles',
               link:'#',
               linkCorrente:false,
            },
            {
               testo:'videos',
               link:'#',
               linkCorrente:false,
            },
            {
               testo:'fans',
               link:'#',
               linkCorrente:false,
            },
            {
               testo:'news',
               link:'#',
               linkCorrente:false,
            },
            {
               testo:'shop',
               link:'#',
               linkCorrente:false,
            },
         ]
      }
    }
   }
</script>

<template>
   <header>
      <nav>
         <figure>
            <img src="../assets/img/dc-logo.png" alt="" style="height: 50px;">
         </figure>
         <ul>
            <li v-for="(element, index) in linkHeader" :key='index'><a :href="element.link" :class="element.linkCorrente ? 'border-link' : ''">{{ element.testo.toUpperCase() }}</a></li>
         </ul>
      </nav>
   </header>
</template>

<style lang="scss" scoped>
   @use '../scss/partials/mixins.scss' as*;
   @use '../scss/partials/variables.scss'as *;
   
   a.border-link{
      position: relative;
      &::after{
         content: '\005F';
         color:  $bg-blu;
         position: absolute;
         top:-360%;
         font-size:100px;
         left: 10%;
      }
   }

   nav{
      @include d-flex;
      width: 80%;
      margin: 0 auto;
      justify-content: space-between;
      padding: 20px;
      ul{
         @include d-flex;
         gap: 20px;
         a{
            font-size:14px;
            color: rgb(84, 75, 70);
            &:hover {
               color:rgb(17, 138, 250);
            }

         }
      }
   }
</style>