<script setup>
    import { ref } from 'vue';
    import SendEvent from './SendEvent.vue';
    import { products } from './WithData.vue';

    const totalValue = ref(0)

    const increment = (price) => {
        const value = totalValue.value + price
        totalValue.value = +value.toFixed(2)
    }

</script>

<template>
    <div class="component">
        <h1>Component that listens an Event</h1>
        <p>Total: R${{ totalValue }}</p>

        <div v-for="product in products" :key="product.id">
            <SendEvent :item="product.name" :price="product.price" @wasAdded="increment"/>
        </div>
    </div>
</template>