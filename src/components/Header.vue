<template>
    <div class="row">
        <div class="col-sm-12">
            <h4>Quotes Added</h4>
            <div class="progress">
            <div class="progress">
                <div class="progress-bar w-75"
                role="progressbar"
                aria-valuenow="60"
                aria-valuemin="0"
                aria-valuemax="100"
                :style="{width: (quoteCount / maxQuotes) * 100 + '%'}"
                >{{ quoteCount }} / {{ maxQuotes }}</div>
             </div>
        </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['quoteCount', 'maxQuotes']
    }
</script>

<style>
    h4 {
        font-family: Arial, Helvetica, sans-serif;
        color: rgb(100, 100, 100);
    }
    .progress-bar {
        background-color: #5ecde0;
        color: rgb(59, 59, 59);
        font-family: Arial, Helvetica, sans-serif;
    }

</style>