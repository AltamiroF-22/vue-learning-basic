<script>
    export const products = [
      { id: 1, name: "Notebook", code: "#562736", price: 3500 },
      { id: 2, name: "Smartphone", code: "#893452", price: 2500 },
      { id: 3, name: "Tablet", code: "#324567", price: 1800 },
      { id: 4, name: "Smartwatch", code: "#981234", price: 1200 },
      { id: 5, name: "Headphone", code: "#564738", price: 600 }
];

const alertProduct = (name, code) => {
  window.alert(`Product name: ${name} & Product code: ${code}`);
};
</script>


<script setup>
const alertProduct = (name, code) => {
window.alert(`product name:${name} & product code: ${code}`)
}
</script>
<template>
    <div class="component">
        <h1>Product list</h1>
        <div class="productCard" @click="alertProduct(product.name, product.code)"
         v-for="product in products":key="product.id">
            <p>Name: {{ product.name }}</p> - Code: {{ product.code }}
        </div>
       
    </div>
</template>

<style scoped>

    .productCard{
        background-color: #222;
        transition: .2s;
        cursor: pointer;
    }

    .productCard:hover{
        background-color: #111;
    }
</style>

    <!-- <script>
    
    //Options API
    // export default {
    //     data:function(){
    //         return{
    //             productName: "notebook",
    //             productCode:"#347823"
    //         }
    //     }
    // }
    
    //Composition API
    // export default {
    //     setup:function(){
    //         const productName = "pen"
    //         const productCode = "#562736"
    //         return{productCode, productName}
    //     }
    // }
    </script> -->