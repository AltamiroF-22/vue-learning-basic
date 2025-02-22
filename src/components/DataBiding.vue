<script setup>
    import { ref } from 'vue';

    const value = ref('vue is very cool');
</script>

<template>
    <div class="component1">
        <h1>Component with bind</h1>
            <!-- <input type="text" v-bind:value="value"> -->
            <!-- <input type="text" :value="value" v-on:input="(e)=> {value=e.target.value}"> -->

            <!-- <input type="text" :value="value" @:input="(e)=> {value=e.target.value}"> -->
            <input type="text" v-model="value">
            <p>Input value: {{ value }}</p>
    </div>
</template>

<style scoped></style>