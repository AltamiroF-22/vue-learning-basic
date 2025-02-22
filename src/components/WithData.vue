<script setup>

const products = [
  { id: 1, name: "Notebook", code: "#562736" },
  { id: 2, name: "Smartphone", code: "#893452" },
  { id: 3, name: "Tablet", code: "#324567" },
  { id: 4, name: "Smartwatch", code: "#981234" },
  { id: 5, name: "Headphone", code: "#564738" }
];

const alertProduct = (name, code) => {
window.alert(`product name:${name} & product code: ${code}`)
}
</script>
<template>
    <div>
        <h1>Product list</h1>
        <div class="productCard" @click="alertProduct(product.name, product.code)"
         v-for="product in products":key="product.id">
            <p>Name: {{ product.name }}</p> - Code: {{ product.code }}
        </div>
       
    </div>
</template>

<style scoped>
    div{
        text-align: center;
        border:  1px solid #e9e9e9;
        background-color: #050d04;
        border-radius: 1em;
        margin: 25px;
        padding: 1em;
    }

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