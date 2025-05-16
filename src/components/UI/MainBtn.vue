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
        :class="`btn-${theme}`"
    >
        <slot />
    </button>
</template>