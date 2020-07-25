<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style>
    .panel-body {
        font-family: 'Lobster', cursive;
        font-weight: 400;
        font-size: 24px;
        color: black;
    }

    .quote {
        cursor: pointer;
    }

    .quote:hover {
        background-color: #328897;
        color: rgb(255, 251, 246);
        box-shadow: .8px .5px grey;
    }
</style>