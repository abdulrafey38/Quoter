<template>
  <div class='container' >

   <appHeader :quoteCount="quotes.length" :maxQuotes="max"></appHeader>
    
    <div class='row'>
      <div class="col-sm-12">
        <newquote @quoteAdded="newQuote"></newquote>
      </div>
    </div>
    <br>
  <appQuoteGrid :quotes='quotes' @deleteevent="quotes.splice($event,1)"></appQuoteGrid>
  <div class="row">
    <div class="col-sm-12 text-center">
      <div class="alert alert-info">
        <strong>Info:</strong>Click on thw quote to delete
      </div>
    </div>
  </div>
   
  </div>
</template>

<script>

import quotegrid from './components/Quotegrid.vue';
import newquote from './components/NewQuote.vue';
import head from './components/header.vue';
export default {
    data:function(){
      return {
        max:10,
        quotes: ['Just a quote to see something']
      }
    },
    components:{
      appQuoteGrid:quotegrid,
      newquote:newquote,
      appHeader:head
    },methods:{
      newQuote(quote){
        if(this.quotes.length>=10)
        {
          return alert('Overload!!! Please Delete Quotes');
        }
         this.quotes.push(quote)

      }
    }
  }

</script>

<style>
</style>
