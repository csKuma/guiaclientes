<template>
  <div id="app">
    <div>
      <h3>cadastro</h3>
      <input type="text" placeholder="nome" v-model="nomeField" />
      <small id="erro" v-show="deuerro"> nome invalido</small> <br />
<input type="number" placeholder="idade" v-model="idadeFeald">
      <button @click="inserir">cadastrar</button>
      <div v-for="cliente in clientes" :key="cliente.id">
        <cliente :cliente="cliente" />
      </div>
    </div>
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
      deuerro: false,
      nomeField:"",
      idadeField: 0,

      clientes: [
        {
          id: 2,
          nome: "felipe",
          idade: 12,
        },
      ],
    };
  },
  methods: {
    inserir: function () {
      if (
        this.nomeField == "" ||
        this.nomeField == " " ||
        this.nomeField.length < 3
      ) {
        this.deuerro = true;
      } else {
        this.clientes.push({
          nome: this.nomeField,
          id: Date.now,
        });
      }
    },
  },
};
</script>
   

<style>
#erro {
  color: red;
}
</style>
