<script setup lang="ts">
import ProductList from './views/ProductList.vue';
</script>

<template>
  <table>
      <tr>
          <th>Product Id</th>
          <th>Product Name</th>
          <th>Product Description</th>
          <th>Product Status</th>
      </tr>
    <ProductList :quantity="0" description="Des jolies fleurs" label="Fleurs"/>
    <ProductList :id="2" :quantity="4" description="Des carottes" label="Carottes"/>
    <ProductList :id="3" :quantity="7" description="Des concombres d'Espagne" label="Concombres"/>
  </table>
</template>

<style></style>