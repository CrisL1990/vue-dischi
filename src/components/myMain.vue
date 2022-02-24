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
            dischi: [],
            generi: []
        }
       
    },

    methods:{

        callApi: function(){

           
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        
            .then((response) => {  
                this.dischi = response.data;
                
                for(let i = 0; i < response.data.response.length; i++){
                    if(!this.generi.includes(response.data.response[i].genre))
                    this.generi.push(response.data.response[i].genre)
                }
                
            })

           

            .catch(function (error) {
                // handle error
                console.log(error);
            })
            console.log(this.generi)
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