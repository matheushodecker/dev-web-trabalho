<script setup>
import { reactive } from 'vue';
const emit = defineEmits(['adicionar']);
const produto = reactive({
    nome: '',
    email: '',
    senha: '',
    Csenha: '',
    DataNascimento: '',
    endereco: '',
    cidade: '',
    estado: '',
    hobbies: '',
    linguagem: '',
    biografia: '',
});
function salvar() {
    if (produto.nome === '' || produto.email === '' || produto.senha === '' || produto.Csenha === '' || produto.DataNascimento === '' || produto.endereco === '' || produto.cidade === '' || produto.estado === '' || produto.hobbies === '' || produto.linguagem === '' || produto.biografia === '') {
        alert('Os campos todos os campos são obrigatórios');
        return;
    }
    emit('adicionar', { ...produto });
}
</script>
<template>
    <form @submit.prevent="salvar">
        <div class="row">
            <label for="nome">nome</label>
            <input type="text" v-model="produto.nome" />
        </div>
        <div class="row">
            <label for="email">email</label>
            <input type="text" v-model="produto.email" />
        </div>
        <div class="row">
            <label for="senha">senha</label>
            <input type="text" v-model="produto.senha" />
        </div>
        <div class="row">
            <label for="Csenha">confirmacao senha</label>
            <input type="text" v-model="produto.Csenha" />
        </div>
        <div class="row">
            <label for="DataNascimento">data nascimento</label>
            <input type="date" v-model="produto.DataNascimento" />
        </div>
        <div class="row">
            <label for="endereco">endereco</label>
            <input type="text" v-model="produto.endereco" />
        </div>
        <div class="row">
            <label for="cidade">cidade</label>
            <input type="text" v-model="produto.cidade" />
        </div>
        <div class="row">
            <label for="estado">estado</label>
            <select name="estado" class="estado" v-model="produto.estado">
                <option value="AC">Acre</option>
                <option value="AL">Alagoas</option>
                <option value="AP">Amapá</option>
                <option value="AM">Amazonas</option>
                <option value="BA">Bahia</option>
                <option value="CE">Ceará</option>
                <option value="DF">Distrito federal</option>
                <option value="ES">Espírito Santo</option>
                <option value="GO">Goiás</option>
                <option value="MA">Maranhão</option>
                <option value="MT">Mato Grosso</option>
                <option value="MS">Mato Grosso do Sul</option>
                <option value="MG">Minas Gerais</option>
                <option value="PA">Pará</option>
                <option value="PB">Paraíba</option>
                <option value="PR">Paraná</option>
                <option value="PE">Pernambuco</option>
                <option value="PI">Piauí</option>
                <option value="RJ">Rio de Janeiro</option>
                <option value="RN">Rio Grande do Norte</option>
                <option value="RS">Rio Grande do Sul</option>
                <option value="RO">Rondonia</option>
                <option value="RR">Roraima</option>
                <option value="SC">Santa Catarina</option>
                <option value="SP">São paulo</option>
                <option value="SE">Sergipe</option>
                <option value="TO">Tocantins</option>
            </select>
        </div>
        <div class="row">
            <label for="hobbies">hobbies</label>
            <input type="text" v-model="produto.hobbies" />
        </div>
        <div class="row">
            <label for="linguagem">linguagem de programação</label>
            <input type="text" v-model="produto.linguagem" />
        </div>
        <div class="row">
            <label for="biografia">biografia</label>
            <input type="text" v-model="produto.biografia" />
        </div>
        <button type="submit">Salvar</button>
    </form>
</template>
<style scoped>
.formulario {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  background: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

input[type="text"],
input[type="email"],
input[type="password"],
input[type="date"],
textarea,
select {
  width: 100%;
  padding: 10px;
  border-radius: 4px;
  border: 1px solid #ccc;
}

textarea {
  resize: vertical;
  height: 100px;
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