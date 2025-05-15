<script setup>
const props = defineProps({
    theme: {
        type: String,
        default: 'orange'
    }
})
</script>

<template>
    <button
        class="main-btn"
        :class="{
            'bg-[#FF9500]': props.theme == 'orange',
        }"
    >
        <slot />
    </button>
</template>