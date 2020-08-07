/* eslint-disable vue/no-unused-vars */
<template>
    <div class='row'>
        
        <app-quote v-for="(quote,index) in quotes" v-bind:key='quote' @click.native='deletequote(index)'>{{ quote }}</app-quote>
    </div>
</template>


<script>
import quote from './Quote.vue';

export default {
    props:['quotes'],
    components:{
        appQuote:quote
    },methods:{
        deletequote(index){
            this.$emit('deleteevent',index);

        }
    }
    
}
</script>


<style  scoped>

</style>