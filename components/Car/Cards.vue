<script setup lang="ts">
const { cars } = useCars()
</script>

<template>
    <!--
<p>debug output</p>
    <p>{{ cars }}</p>
-->
    <div class="w-full">
        <CarCard v-for="car in cars" :key="car.id" :car="car" />
    </div>
</template>