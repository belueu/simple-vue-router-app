<script setup>
import { RouterLink } from "vue-router"

</script>

<template>
    <div class="container">
        <div>
            <RouterLink active-class="active" to="/">Home</RouterLink>
        </div>
        <div>
            <RouterLink active-class="active" to="/about">About</RouterLink>
        </div>
    </div>
</template>

<style scoped>
.active {
    font-weight: 900;
    color: cadetblue;
}

.container {
    display: flex;
    margin: 20px;
}

.container div {
    display: flex;
    margin: 10px;
}
</style>