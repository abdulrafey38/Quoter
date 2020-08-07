<template>
    <div class='row'>
        <app-quote v-for="quote in quotes" v-bind:key='quote'>{{ quote }}</app-quote>
    </div>
</template>


<script>
import quote from './Quote.vue';

export default {
    props:['quotes'],
    components:{
        appQuote:quote
    }
    
}
</script>


<style  scoped>

</style>