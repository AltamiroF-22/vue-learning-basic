<script setup>
// import {watch} from 'vue';
import { ref} from 'vue';
import { watchEffect } from 'vue';

const bornIN = ref(2002)
const currentYear = ref(2030)
const age = ref(0)

// watch(currentYear, (year)=> {
//     age.value = year - bornIN.value
// })

// watch(bornIN, (year)=> {
//     age.value = currentYear.value - year
// })

watchEffect(()=> {
    age.value = currentYear.value - bornIN.value
})

</script>

<template>
    <div class="component">
        <h1>Component with <span> Assited</span> Computed Properties</h1>
       <p>Current age: {{ age }}</p>

       <div class="year">
     <div class="">
        <label for="year">Born in:</label>
        <input type="number" v-model="bornIN">
     </div>
<div class="">
    
    <label for="year">Current year:</label>
        <input type="number" v-model="currentYear">
</div>
       </div>
    </div>
</template>


<style scoped>
    p{
        font-size: 2rem;
    }

    .year{
        display:  flex;
        align-items: center;
        justify-content: center;
    }
    input{
        width: 90%;
    }
    label{
        font-size: 1.5rem;
    }

    span {
        color: orange;
    }
</style>