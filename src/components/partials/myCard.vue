<template>
    <div class="card">
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
        width: 12rem;
        margin: 10px 20px;
        background-color: rgb(46, 58, 70);

        img{
            margin-top: 15px;
           
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