<template>
    <div class="col">
        <img :src="disco.poster" alt="">
        <h2>{{disco.title}}</h2>
        <div>{{disco.author}}</div>
        <div>{{disco.year}}</div>
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

</style>