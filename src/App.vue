<script setup>
import { ref } from 'vue'
import FormulariosWiew from './components/FormulariosWiew.vue'
import ResultadoWiew from './components/ResultadoWiew.vue'
const mostrarResultado = ref(false)
const produtos = ref([

]);
const proxId = ref(1);

function adicionarProduto(produto) {
  produto.id = proxId;
  produtos.value.push(produto);
  proxId.value++;
}
</script>

<template>
  <div class="container">
    <div v-if="!mostrarResultado" class="formularios">
      <h1>formularios</h1>
      <FormulariosWiew @adicionar="adicionarProduto" />
      <button @click="mostrarResultado = true">mostrar</button>
    </div>
    <div v-else class="resultado">
      <h2>resultados</h2>
      <ResultadoWiew :produtos="produtos" />
      <button @click="mostrarResultado = false">mostrar</button>
    </div>

  </div>
</template>

<style scoped>
.app-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.section {
  margin-bottom: 20px;
}

button {
  background-color: #4CAF50;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}
</style>