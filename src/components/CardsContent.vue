<script>
    export default{
        name:'CardsContent',
        props:{
           propsThumb:String,
            propsSeries:String,
        },
        data(){
            return{
               
            }
        }
    }

</script>

<template>
    <div class="card">
        <figure>
            <img :src="propsThumb" alt="" style="height: 250px;">
        </figure>
        <h4>{{ propsSeries }}</h4>
    </div>

</template>

<style lang="scss" scoped>
    .card{
        flex-basis: calc(100% / 6 - 10px - 10px);
        figure{
            width: 100%;
            img{
                width: 100%;
                display: block;
            }
        }
    }
    h4{
        text-transform: uppercase;
        color: white;
    }
</style>