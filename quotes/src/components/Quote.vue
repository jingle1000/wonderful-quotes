<template>
    <div class="card col-3 shadow p-4">
        <p class="mx-auto">
            <slot></slot>
        </p>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
p {
    font-family: cursive;
}
.card:hover {
    background: rgb(255, 193, 193);
}
</style>
