<script setup>
    const props = defineProps(['realizaOperacao'])
</script>

<template>
    <h2 class="d-flex justify-content-center">O resultado é:</h2>
    <h1 class="d-flex justify-content-center">{{ props.realizaOperacao }}</h1>
</template>