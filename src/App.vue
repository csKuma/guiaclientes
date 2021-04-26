<template>
  <div id="app">
    <input type="text" v-model="clientevictor.nome" />
    <cliente :cliente="clientevictor" :showIdade="false" />
  </div>
</template>

<script>
import cliente from "./components/cliente.vue";
export default {
  name: "App",
  components: {
    cliente,
  },
  data() {
    return {
      clientevictor: {
        nome: "victor feio",
        idade: 14
      },
    };
  },
};
</script>
   

<style>
</style>
