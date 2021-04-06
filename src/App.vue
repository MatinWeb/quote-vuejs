<template lang="">
  <div class="container mt-3">
    <app-header :quoteCount="quoteCounted" :maxQuote="maximumQuote"></app-header>
    <app-add-quote @quoteAdded="addNewQuote"></app-add-quote>
    <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>
<script>
import quoteGrid from "./components/quote-grid";
import addquote from './components/addquote.vue';
import header from './components/progressBar.vue'
export default {
  data() {
    return {
      quotes: ["the first QUOTE"],
      maximumQuote: 10,
    };
  },
  computed:{
    quoteCounted(){
      return this.quotes.length
    }
  },
  methods:{
    addNewQuote(quote){
      if(this.quoteCounted >= 10){
        return alert('Please delete Quotes first!')
      }
      this.quotes.push(quote);
    }
  },
  components: {
    appAddQuote: addquote,
    appQuoteGrid: quoteGrid,
    appHeader: header,
  },
};
</script>
<style lang="">
</style>