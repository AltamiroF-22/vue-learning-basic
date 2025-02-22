<template>
    <div class="component">
        <h1>component with primitive reactive data</h1>
        <p>Name:{{ name }} | Age: {{ age }}</p>
        <button v-on:click="changeName()">change name</button>
        <button @click="birthday()">birthday</button>

    </div>
</template>


<script setup>
    import {ref} from 'vue'

    const name = ref("Junior")
    const age = ref(22)

    const birthday = () => {
        age.value += 1
    }

    const changeName = () => {
        name.value = "junior rocha"
    }
</script>



<style scoped>

button{
    padding: 1em;
    border-radius: 5px;
    cursor: pointer;
}
</style>