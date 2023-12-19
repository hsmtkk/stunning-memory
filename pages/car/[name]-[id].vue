<script setup lang="ts">
const route = useRoute()
const car = await useFetchCar(route.params.id)
const { toTitleCase } = useUtilities()

useHead({
    title: toTitleCase(route.params.name),
})

if (!car) {
    throw createError({
        statusCode: 404,
        message: `Car with ID of ${route.params.id} does not exist`,
    })
}

definePageMeta({
    layout: "custom",
})

</script>

<template>
    <div v-if="car">
        <CarDetailHero v-bind:car="car" />
        <CarDetailAttribute v-bind:features="car.features" />
        <CarDetailDescription v-bind:description="car.description" />
        <CarDetailContact />
    </div>
</template>