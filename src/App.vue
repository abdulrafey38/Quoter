<template>
  <div class='container' >
    <appQuoteGrid :quotes='quotes'></appQuoteGrid>
   
  </div>
</template>

<script>

import quotegrid from './components/Quotegrid.vue';

export default {
    data:function(){
      return {
        max:10,
        quotes: ['Just a quote to see something','Another Beautiful Quote More to Come']
      }
    },
    components:{
      appQuoteGrid:quotegrid
    }
  }

</script>

<style>
</style>
