<script setup lang="ts">
definePageMeta({
    layout: "custom",
    middleware: ["auth"],
})
</script>

<template>
    <div class="rounded shadow mt-20">
        <CarMessageCard />
    </div>
</template>