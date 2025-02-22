<script setup>
import FirstComponent from './components/FirstComponent.vue';
import WithData from './components/WithData.vue'
import WithPrimitiveReactiveData from './components/WithPrimitiveReactiveData.vue';
import WithNonPrimitiveReactiveData from './components/WithNon-PrimitiveReactiveData.vue';
import DataBiding from './components/DataBiding.vue';
import WithProps from './components/WithProps.vue';
import ListenEvent from './components/ListenEvent.vue';
import ComputedProperties from './components/ComputedProperties.vue';

import { products } from './components/WithData.vue';
</script>

<template>
  <header>
    Vue
  </header>

  <ComputedProperties/>
  <ListenEvent/>


 <div class="with-props">
  <div v-for="product in products" :key="product.id">
    <WithProps :item="product.name" :price="product.price"/>
  </div>
 </div>

  <DataBiding/>
  <WithNonPrimitiveReactiveData/>
  <WithPrimitiveReactiveData/>
  <WithData/>
  <FirstComponent/>

</template>