<script setup>
import { useRoute, useRouter, RouterView } from "vue-router"
import cars from "../data/cars.json"

const route = useRoute()
const router = useRouter()

const carId = parseInt(route.params.id)

const car = cars.find(c => c.id === carId)

</script>

<template>
    <div v-if="car">
        <h1>Car View</h1>
        <p>Manufacturer: {{ car.name }}</p>
        <p>Year: {{ car.year }}</p>
        <p>Price: {{ car.price }}</p>
        <button @click="router.push(`/cars/${carId}/contact`)">Show Contact Info!</button>
        <RouterView />
    </div>
    <div v-else>
        <h2>Sorry, the car that you are loking for does not exist!!!</h2>
    </div>

</template>