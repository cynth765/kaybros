<template>
    <div class=" p-2 rounded mt-2">
        <div v-on:click="isOpen = !isOpen" class="bg-slate-300 text-zinc-500 p-6 font-bold rounded cursor-pointer pl-2">{{ title }}</div>
        <div class="mt-4 " :class="isOpen ? 'd-block' : 'hidden'">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    data: () => {
        return {
            isOpen: false
        }
    },
    name: 'Accordion',
    props: {
        title: String,
    }
}
</script>