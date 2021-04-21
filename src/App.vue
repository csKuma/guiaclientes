<template>
  <div id="app">
    <h1>GUIA DE COISAS </h1>
    <clientes/>
    <produto/>
  
  </div>
</template>

<script>
  import clientes from "./components/clientes";
import Produto from './components/produto.vue';
export default {
  name: 'App',
  components:{
    clientes,
    Produto
  }
}
</script>
   

<style>

</style>
