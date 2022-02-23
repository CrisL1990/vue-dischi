<template>
    <main class="container">
        <div class="row">

        </div>
    </main>
  
</template>

<script>

const axios = require('axios');
export default {
    name: 'myMain',

    data(){
        return{
            myArray: []
        }
       
    },

    methods:{

        callApi: function(){

            axios.get('https://flynn.boolean.careers/exercises/api/array/music')

            .then((response) => {
                
                this.myArray = response.data;
                console.log(this.myArray);
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

</style>