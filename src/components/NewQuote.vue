<template>
    <div class='row'>
        <app-quote v-for="quote in quotes" v-bind:key='quote'>{{ quote }}</app-quote>
    </div>
</template>


<script>


export default {
   
    
}
</script>


<style  scoped>

</style>