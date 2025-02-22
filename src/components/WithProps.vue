<script setup>
import { defineProps } from 'vue';

defineProps({
    item:String,
    price:Number
})

</script>

<template>
<div class="component product">
    <h1>Component with props</h1>
    <p>{{ item }} (R${{ price.toFixed(2)}})</p>
</div>
</template>


<style scoped>
.product{
    min-width:200px ;
    padding: 0 100px;
}
</style>