<template>
  <div :class="cliente">
    <p>nome:{{ cliente.nome }}</p>
    <p v-if="showIdade == false">idade{{ cliente.idade }}</p>
    
    <p v-else>escondeu a idade</p>
    <button @click="esconder">esconder idade</button>
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
  },
  methods:{
    esconder: function(){
      this.showIdade=!this.showIdade;
    }
  }
  
}
</script>

<style scoped>
</style>