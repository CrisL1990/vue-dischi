<template>
    <main class="container">
        <div class="row">
            <myCard v-for="(disco, index) in dischi.response" 
            :key="index"
            :disco="disco"
            />
        </div>
    </main>
  
</template>

<script>

const axios = require('axios');

import myCard from './partials/myCard.vue'

export default {
    name: 'myMain',

    components:{
        myCard,
    },

    data(){
        return{
            dischi: []
        }
       
    },

    methods:{

        callApi: function(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')

            .then((response) => {  
                this.dischi = response.data;
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            })
        }
    },

    created(){
        this.callApi();
    }
}
</script>

<style scoped lang="scss">

    .container{
        padding: 50px 0;
    }
</style>