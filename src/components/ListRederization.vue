<script setup>
    import { defineProps } from 'vue';
    defineProps({
        name: String,
        dogs: Array
    })
</script>

<template>
    <div class="component">
        <h1>Component with  list redering</h1>
        <p>Name: {{ name }}</p>
        <p v-show="dogs.length === 0">Does not have dogs</p>
        <ul>
            <li v-for="dog in dogs" :key="dog.id">
                Name: {{ dog.name }} | Age: {{ dog.age }}
            </li>
        </ul>
    </div>
</template>