<script setup>
    import { defineProps } from 'vue';
    defineProps({
        name: String,
        dogsQuantity: Number
    })
</script>

<template>
    <div class="component">
        <h1>Component with condicional redering</h1>
        <p>Name: {{ name }}</p>

        <p v-if="dogsQuantity === 0">Does not have dogs</p>
        <p v-else-if="dogsQuantity === 1">have one dog</p>
        <p v-else>have {{ dogsQuantity }} dogs</p>
    </div>
</template>