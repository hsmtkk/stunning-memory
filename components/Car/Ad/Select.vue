<script setup lang="ts">
const props = defineProps({
    title: String,
    name: String,
    options: Array,
})

const emits = defineEmits(["changeInput"])
const state = ref("")

const onChange = () => {
    emits("changeInput", state.value, props.name)
}
</script>

<template>
    <div class="flex flex-col w-[48%] mt-2">
        <label class="text-cyan-500 mb-1 text-sm">{{ title }}</label>
        <select class="p-2 border w-100 rounded" v-on:click="onChange" v-model="state">
            <option v-for="option in options" v-bind:key="option" v-bind:value="option">{{ option }}</option>
        </select>
    </div>
</template>