<template>
  <div class="about">
    <h1 id="eae"> eae cebola {{ nome }}</h1>

    <p>
      <label for="nome" id="labelName">Nome:</label>
    <input id="nome" type="text" v-model="nome">
    <input type="text" :value="nome" @input="alteraNome">

    </p>
    <p v-if="nome.length<5">ELIZABERTO GODOFREDO</p>
    <p v-else>NOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO</p>

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

  
const nome = ref("JOVEM")

const usuarios = ref([{nome: "JEFERSON", senha:"123456"}, {nome: "CAMINHOES", senha:"EUROTRUCK"}])

function alteraNome(e: any) {
  nome.value = e.target.value;
}

function addUser() {

}



</script>
