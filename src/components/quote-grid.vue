<template lang="">
    <div class="row">
        <!-- baray remove az tarigh click rooye kole component -->
        <!-- <app-quote v-for="(quote, index) in quotes" @click.native="removeQuote(index)">{{ quote }}</app-quote> -->
        <app-quote v-for="(quote, index) in quotes" @removeThisQuote="removeQuote(index)">{{ quote }}</app-quote>
    </div>
</template>

<script>
import quote from "./quote.vue";
export default {
  props: ["quotes"],
  methods: {
    removeQuote(index) {
    //   debugger;
      this.quotes.splice(index, 1);
    },
  },
  components: {
    appQuote: quote,
  },
};
</script>