<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
    item:String,
    price:Number
})

const emit = defineEmits(["wasAdded"])

const add = () => {
    emit('wasAdded', props.price)
}

</script>

<template>
<div class="component">
    <h1>Component that emits an event</h1>
    <p>{{ item }} (R$:{{ price.toFixed(2) }})</p>
    <button @click="add">Add to cart</button>
</div>
</template>

