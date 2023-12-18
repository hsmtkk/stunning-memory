<script setup lang="ts">
definePageMeta({
    layout: "custom",
})

const supabase = useSupabaseClient()

const user = useSupabaseUser()

const login = async () => {
    const { error } = await supabase.auth.signInWithOAuth({
        provider: "google",
        options: {
            queryParams: {
                access_type: 'offline',
                prompt: 'consent',
            },
        }
    })
    if (error) {
        console.log(error)
    }
}
</script>

<template>
    <div class="mt-10">
        <h1 class="text-5xl font-bold mb-7">
            Log in
        </h1>
        <button v-on:click="login" class="bg-red-400 p-3 rounded text-white font-bold">Login with Google</button>
    </div>
</template>