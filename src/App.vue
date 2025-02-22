<script setup>
import FirstComponent from './components/FirstComponent.vue';
import WithData from './components/WithData.vue'
import WithPrimitiveReactiveData from './components/WithPrimitiveReactiveData.vue';
import WithNonPrimitiveReactiveData from './components/WithNon-PrimitiveReactiveData.vue';
import DataBiding from './components/DataBiding.vue';
</script>

<template>
  <header>
    Vue
  </header>
  <DataBiding/>
  <WithNonPrimitiveReactiveData/>
  <WithPrimitiveReactiveData/>
  <WithData/>
  <FirstComponent/>
</template>

<style scoped>

</style>
