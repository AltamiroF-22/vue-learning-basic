<script setup>
import FirstComponent from './components/FirstComponent.vue';
import WithData from './components/WithData.vue'
import WithPrimitiveReactiveData from './components/WithPrimitiveReactiveData.vue';
</script>

<template>
  <header>
    Vue
  </header>
  <WithPrimitiveReactiveData/>
  <WithData/>
  <FirstComponent/>
</template>

<style scoped>

</style>
