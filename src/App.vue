<script setup>
//Importando funcion
//para crear referencias reactivas
import {ref } from 'vue'
// Creando una referencia reactiva
// de tipo string 
const header =ref('App lista de compras');
const shoppingIcon=ref('material-icons shopping-cart-icon')
// Creando una referencia reactiva
// para almacenar el valor de la lista 
const items = ref([
    {id: 0 , label:'Leche'},
    {id: 1 , label:'Arroz'},
    {id: 2 , label:'Carne'},
    {id: 3 , label:'Pan'},
    {id: 4 , label:'Huevos'}
]);
//Creando variable reactiva 
const newItem=ref('');
</script>

<template>
<h1><i :class="shoppingIcon">local_mall</i>{{ header }}</h1>
<input v-model="newItem"  type="text" placeholder="Agregar Articulo">
<ul>
    <li v-for="{id , label } in items" v-bind:key="id">⭐ {{label}}</li>
</ul>

</template>

<style scoped>
.shopping-cart-icon {
    font-size: 2rem;
}
</style>
