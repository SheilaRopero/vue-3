<script setup>
import { ref } from 'vue';

let producto = ref([
  {nombre  : 'mantequilla' , cantidad :ref(3), precio : ref(400), },
  {nombre  : 'pan',cantidad:ref(2),precio:ref(1500)},
  { 
    nombre:'leche', cantidad : ref (3), precio : ref(4000) },
    
])







</script>

<template>
  
  <div>
    <h1>carrito de compras</h1>

  <div v-for="productos,index in producto" :key="index" >
  <label for="cantidad-producto">cantidad de producto:</label>
    <input type="number" v-model="productos.cantidad" /> 

    <label for="cantidad-producto">precio producto:</label>
    <input type="number" v-model="productos.precio" /> 
   
   
<div>
  
  <table>
        <tr>
          <td >Nombre Producto</td>
          <th>{{ productos.nombre  }}</th>
        </tr>
  
        <tr>
          <td>Cantidad Producto</td>
          <th>{{ productos.cantidad }}</th>
        </tr>
  
        <tr>
          <td>Precio Producto</td>
          <th>{{ productos.precio }}</th>
        </tr>
  
        <tr>
          <td>Valor Producto</td>
          <th>{{ productos.precio *  productos.cantidad}}</th>
        </tr>
      </table>
</div>
    </div>
  </div>
  
  <h2>Valor Total: {{ valorTotal }}</h2>
  
</template>

<style scoped>
h1{
  text-align: center;
  color: rgb(25, 94, 94);
  font-family: sans-serif;
}

</style>
