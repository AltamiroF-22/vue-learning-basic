<script setup>
import FirstComponent from './components/FirstComponent.vue';
import WithData from './components/WithData.vue'
import WithPrimitiveReactiveData from './components/WithPrimitiveReactiveData.vue';
import WithNonPrimitiveReactiveData from './components/WithNon-PrimitiveReactiveData.vue';
import DataBiding from './components/DataBiding.vue';
import WithProps from './components/WithProps.vue';
import ListenEvent from './components/ListenEvent.vue';
import ComputedProperties from './components/ComputedProperties.vue';
import AssitedComputedProperties from './components/AssitedComputedProperties.vue';
import CondicionalRedering from './components/CondicionalRedering.vue';
import ListRederization from './components/ListRederization.vue';
import Slots from './components/Slots.vue';

import { products } from './components/WithData.vue';
</script>

<template>
  <header>
    Vue
  </header>

  <Slots>
    <template v-slot:icon>
      <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="currentColor"  class="icon icon-tabler icons-tabler-filled icon-tabler-accessible"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M17 3.34a10 10 0 1 1 -14.995 8.984l-.005 -.324l.005 -.324a10 10 0 0 1 14.995 -8.336zm-1.051 6.844a1 1 0 0 0 -1.152 -.663l-.113 .03l-2.684 .895l-2.684 -.895l-.113 -.03a1 1 0 0 0 -.628 1.884l.109 .044l2.316 .771v.976l-1.832 2.75l-.06 .1a1 1 0 0 0 .237 1.21l.1 .076l.101 .06a1 1 0 0 0 1.21 -.237l.076 -.1l1.168 -1.752l1.168 1.752l.07 .093a1 1 0 0 0 1.653 -1.102l-.059 -.1l-1.832 -2.75v-.977l2.316 -.771l.109 -.044a1 1 0 0 0 .524 -1.221zm-3.949 -4.184a1.5 1.5 0 1 0 0 3a1.5 1.5 0 0 0 0 -3z" /></svg>
    </template>

   <template v-slot:text>
    Something
   </template>
  </Slots>

  <ListRederization name="Junior" 
  :dogs="[
    {name: 'dog1', id: '1212', age: 7},
    {name: 'dog2', id: '12', age: 3}
    ]"/>

  <CondicionalRedering name="junior" :dogsQuantity="5"/>
  <AssitedComputedProperties/>
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