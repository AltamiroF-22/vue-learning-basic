<template>
    <div class="component">
        <h1>component with non-primitive reactive data</h1>
        <p>Name:{{ person.name }} | Age: {{ person.age}}</p>
        <button v-on:click="changeName()">change name</button>
        <button @click="birthday()">birthday</button>

    </div>
</template>


<!-- <script setup>
    import {reactive} from 'vue'

    const person = reactive({name:'junior', age: 22})

    const birthday = () => {
        person.age+= 1
    }

    const changeName = () => {
     person.name = "junior rocha"
    }
</script> -->

<script>
export default {
    data:function(){
        return{
            person:{
                name:'Altamiro',
                age: 22,
            }
        }
        
    },

    methods:{
        birthday: function(){
            this.person.age += 1
        },
        changeName: function(){
            this.person.name = 'Altamiro ferrari'
        }
    }

}
</script>

<style scoped>

button{
    padding: 1em;
    border-radius: 5px;
    cursor: pointer;
}
</style>