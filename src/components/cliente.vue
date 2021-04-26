<template>
  <div id="cliente">
    <p>nome:{{cliente.nome}}</p>
  <p v-if="showIdade==true">idade{{cliente.idade}}</p>
  <p v-else>escondeu a idade</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
     }
  },
  props:{
    cliente: Object,
    showIdade:Boolean,
    
  }
  
}
</script>

<style scoped>
</style>