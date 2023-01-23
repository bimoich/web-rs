<template>
    <div>
        <p>Product Details | Id: {{ id }}</p>
    </div>
</template>

<script setup>
const { id } = useRoute().params
definePageMeta({
    layout: 'products'
})
</script>

<style scoped>

</style>