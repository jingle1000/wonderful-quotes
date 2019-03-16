<template>
    <div>
        <div class="progress-bar-container mb-4">
            <div class="progress-bar bg-primary" :style="{width: (quotes/maxQuotes)*100+'%'}"></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "progressBar",
        props: ["quotes", "maxQuotes"],
    }
</script>

<style>
    .progress-bar-container {
        margin: 30px;
        height: 40px;
        background-color: #333;
        padding: 0;
    }
    .progress-bar {
        height: 100%;
    }
</style>