<script setup>
import FirstComponent from './components/FirstComponent.vue';
import WithData from './components/WithData.vue'
import WithPrimitiveReactiveData from './components/WithPrimitiveReactiveData.vue';
import WithNonPrimitiveReactiveData from './components/WithNon-PrimitiveReactiveData.vue';
import DataBiding from './components/DataBiding.vue';
import WithProps from './components/WithProps.vue';

import { products } from './components/WithData.vue';
</script>

<template>
  <header>
    Vue
  </header>

 <div class="with-props">
  <div v-for="product in products" :key="product.id">
    <WithProps :item="product.name" :price="price=product.price"/>
  </div>
 </div>

  <DataBiding/>
  <WithNonPrimitiveReactiveData/>
  <WithPrimitiveReactiveData/>
  <WithData/>
  <FirstComponent/>

</template>

<style scoped>

</style>
