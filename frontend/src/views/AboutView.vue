<template>
  <div class="about">
    <h1 id="eae"> Eae</h1>

    <p>
      <label for="nome" id="labelName">Nome:</label>
    <input id="nome" type="text" v-model="nome">
    <input type="text" :value="nome" @input="alteraNome">
    </p>
    <p>
      <label for="senha" id="labelName">Senha:</label>
    <input id="senha" type="text" v-model="senha">
    <input type="text" :value="nome" @input="alteraNome">
    </p>
    <button @click="addUser">Incluir</button>

    <table>
      <thead>
        <th>
          Nome
          Senha
        </th>
      </thead>
      <tbody>
        <tr v-for="usuario in usuarios">
          <td>{{usuario.nome}}</td>
          <td>{{usuario.senha}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>




<script setup lang="ts">
import { ref } from 'vue';

  
const nome = ref("JOVEM");
const senha = ref("sadboi");

const usuarios = ref([{nome: "JEFERSON", senha:"123456"}, {nome: "CAMINHOES", senha:"EUROTRUCK"}])

function alteraNome(e: any) {
  nome.value = e.target.value;
}

function addUser() {

}



</script>
