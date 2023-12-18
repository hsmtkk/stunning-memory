<script setup lang="ts">
const supabase = useSupabaseClient()

const user = useSupabaseUser()

const logout = async () => {
    const { error } = await supabase.auth.signOut()
    if (error) {
        console.log(error)
    }
    navigateTo("/")
}
</script>

<template>
    <header class="sticky top-0 z-50 flex justify-between items-center space-x-1 border-b bg-white p-4 shadow-md">
        <NuxtLink v-bind:to="{ name: 'index' }" class="text-3xl font-mono">cartrader</NuxtLink>
        <div v-if="user" class="flex">
            <NuxtLink v-bind:to="{ name: 'profile-listings' }" class="mr-5">profile</NuxtLink>
            <p class="cursor-pointer" v-on:click="logout">Logout</p>
        </div>
        <div v-else>
            <NuxtLink v-bind:to="{ name: 'login' }">Login</NuxtLink>
        </div>
    </header>
</template>