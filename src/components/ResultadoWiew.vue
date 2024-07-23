<script setup>
import { reactive } from 'vue'

const produto = reactive({
  nome: 'nome',
  email: 'email',
  senha: 'senha',
  Csenha: 'confirmacao senha',
  DataNascimento: 'data nascimento',
  endereco: 'endereco',
  cidade: 'cidade',
  estado: 'estado',
  hobbies: 'hobbies',
  linguagem: 'linguagem programação',
  biografia: 'biografia'
})
</script>

<template>
  <div class="container">
    <div class="resultado">
      <h2>resultados</h2>

      <p>nome: {{ produto.nome }}</p>
      <p>email: {{ produto.email }}</p>
      <P>senha: {{ produto.senha }}</P>
      <p>Csenha: {{ produto.Csenha }}</p>
      <p>Data: {{ produto.DataNascimento }}</p>
      <p>endereco: {{ produto.endereco }}</p>
      <p>cidade: {{ produto.cidade }}</p>
      <p>estado: {{ produto.estado }}</p>
      <p>hobbies: {{ produto.hobbies }}</p>
      <p>linguagem: {{ produto.linguagem }}</p>
      <p>biografia: {{ produto.biografia }}</p>
      <p>{{ mostrarResultado }}</p>
      <button @click="mostrarResultado = false">mostrar</button>
    </div>
  </div>
</template>

<style scoped>
template {
  background-color: black;
}
.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 1.5rem;
  width: 100vw;
  padding: 25vh 5vh;
}

.formularios,
.resultado {
  width: 45%;
  border-radius: 10px;
  padding: 25px;
}

.formularios {
  background-color: #c4c500;
}

.row {
  margin: 10px 20px;
  width: 70%;
  display: flex;
  justify-content: space-between;
}

.resultado {
  background-color: #c4c4c4;
}
</style>
