<script setup>
defineProps(['produtos']);

</script>

<template>
    <table>
        <tbody>
            <tr v-for="produto in produtos" :key="produto.id">

                <td>nome: {{ produto.nome }}</td>
                <td>email: {{ produto.email }}</td>
                <td>senha: {{ produto.senha }}</td>
                <td>Csenha: {{ produto.Csenha }}</td>
                <td>Data: {{ produto.DataNascimento }}</td>
                <td>endereco: {{ produto.endereco }}</td>
                <td>cidade: {{ produto.cidade }}</td>
                <td>estado: {{ produto.estado }}</td>
                <td>hobbies: {{ produto.hobbies }}</td>
                <td>linguagem: {{ produto.linguagem }}</td>
                <td>biografia: {{ produto.biografia }}</td>
                <td>{{ mostrarResultado }}</td>

            </tr>
        </tbody>
    </table>
</template>

<style scoped>
.resultado-table {
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-bottom: 20px;
}

thead {
  background-color: #f4f4f4;
}

th, td {
  padding: 12px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}

th {
  background-color: #4CAF50;
  color: white;
}
</style>