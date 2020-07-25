<template>
    <div class="row">    
        <form>
            <div class="form-group col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
                <label>Write your new quote here</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <div class="form-group col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
                <button class="btn" @click.prevent="createNew">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                quote: ''
            }
        },
        methods: {
            createNew() {
                this.$emit('quoteAdded', this.quote);
                this.quote = '';
            }
        }
    }
</script>

<style>
    .btn {
        font-family: Arial, Helvetica, sans-serif;
        background-color: #5ecde0;
        color: rgb(59, 59, 59);
    }

    .btn:hover {
        background-color: #328897;
        color: rgb(248, 248, 248);
    }

    label {
        font-family: Arial, Helvetica, sans-serif;
        font-weight: 600;
        color: rgb(100, 100, 100);
    }
</style>