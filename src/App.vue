<template>
    <div class="container">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <app-new-quote @quoteAdded="newQuote"></app-new-quote> 
        <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">CLICK ON A QUOTE TO DELETE IT</div>
            </div>
        </div>
    </div>
</template>

<script>
    import NewQuote from './components/NewQuote.vue';
    import QuoteGrid from './components/QuoteGrid.vue';
    import Header from './components/Header.vue';
    
    export default {
        data: function () {
            return {
                quotes: [
                'This is just a Quote to see someting.'
                ],
                 maxQuotes: 10
            }
        },
        methods: {
            newQuote(quote) {
                if (this.quotes.length >= this.maxQuotes) {
                    return alert('Please delete quotes first!');
                }
                this.quotes.push(quote);
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1);
            }
        },
        components: {
            appQuoteGrid: QuoteGrid,
            appNewQuote: NewQuote,
            appHeader: Header
        }
    }
</script>

<style>
    .alert-info {
        background-color: #5ecde0;
        color: rgb(59, 59, 59);
        font-family: Arial, Helvetica, sans-serif;
    }

</style>
