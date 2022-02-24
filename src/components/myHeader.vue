<template>
    <header class="d-flex justify-content-end align-items-center px-5">
        <mySelect />
    </header>
    
</template>

<script>
import mySelect from './partials/mySelect.vue'
export default {
    name: 'myHeader',
    
    components:{
        mySelect
    },

}
</script>

<style scoped lang="scss">
    header{
        width: 100%;
        height: 80px;
        background-color: rgb(46, 58, 70);
        
    }
    

</style>