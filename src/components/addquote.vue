<template lang="">
    <div class="row">
        <div class="col-xs-12 col-sm-8 offset-sm-2 col-md-6 offset-md-3 form-group">
            <label>Quote</label>
            <textarea class="form-control" rows="3" v-model="newQuote" placeholder="ADD NEW QUOTE"></textarea>
        </div>
        <div class="col-xs-12 col-sm-8 offset-sm-2 col-md-6 offset-md-3 form-group">
            <button class="btn btn-primary" @click.prevent="addNewQuote">Add Quote</button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            newQuote: ''
        }
    },
    methods:{
        addNewQuote(){
            // debugger;
            this.$emit('quoteAdded', this.newQuote);
            this.newQuote = ''
        }
    }
}
</script>