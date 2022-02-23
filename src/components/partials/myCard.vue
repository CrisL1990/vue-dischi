<template>
<!--
     <div class="col">
        <img :src="disco.poster" alt="">
        <h2>{{disco.title}}</h2>
        <div>{{disco.author}}</div>
        <div>{{disco.year}}</div>
    </div>
-->

    <div class="card" style="width: calc(20% - 40px);">
        <img :src="disco.poster" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title title">{{disco.title}}</h5>
            <p class="card-text">{{disco.author}}</p>
            <p class="card-text">{{disco.year}}</p>
        </div>
    </div>
   
</template>

<script>
export default {
    name: 'myCard',

    props:{
        'disco': Object
    },
}
</script>

<style scoped lang="scss">

    .card{
        margin: 10px 20px;
        background-color: rgb(46, 58, 70);

        img{
            margin-top: 15px;
            width: 100%;
            height: 100%;
        }

        .title{
            text-align: center;
            color: white;
        }

        p{
            text-align: center;
            color: rgb(128, 128, 120);
        }
    }    

</style>