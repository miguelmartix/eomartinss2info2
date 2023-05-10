<script setup>
import { ref } from 'vue'
const nome = ref('')
const data = ref('')
const email = ref('')
const endereco = ref('')
const cidade = ref('')
const estado = ref('')
const Hobbie = ref([])
const linguagem = ref('')
const biografia = ref('')
const senha = ref('')
const confirma = ref('')
const ok = ref(false)
</script>

<template>

  <div>
    <div class = "box">
      <form action="">
       <fieldset>
        <legend>Formulário</legend>
        <button>Nome:</button>
       <input type="text" v-on:keypress="ok=false" v-model="nome" placeholder="Digite seu nome" class="labelImput" />
       <hr>
       <button>Email:</button>
       <input type="email" v-on:keypress="ok=false" v-model="email" placeholder="Digite seu email"  class="labelImput" />
       <hr>
       <button>Senha:</button>
       <input type="password" v-on:keypress="ok=false" v-model="senha" placeholder="Digite sua senha"  class="labelImput" />
       <hr>
       <button>Confirmação de senha:</button>
       <input type="password" v-on:keypress="ok=false" v-model="confirma" placeholder="Digite sua senha novamente"  class="labelImput" />
       <hr>
       <button>Data de nascimento:</button>
       <input type="text" v-on:keypress="ok=false" v-model="data" placeholder="Digite sua data"  class="labelImput" />
       <hr>
       <button>Endereço:</button>
       <input type="text" v-on:keypress="ok=false" v-model="endereco" placeholder="Digite seu endereço"  class="labelImput" />
       <hr>
       <button>Cidade:</button>
       <input type="text" v-on:keypress="ok=false" v-model="cidade" placeholder="Digite sua cidade"  class="labelImput" />
       <hr>
       <button>Hobbie:</button>
       <input type="text" v-on:keypress="ok=false" v-model="Hobbie" placeholder="Digite seu hobbie"  class="labelImput" />
        <div>
          <label for="Esportes">Esportes</label>
          <input type="checkbox" v-model="Hobbie" value="Esportes" />;
          <label for="Musica">Música</label>
          <input type="checkbox" v-model="Hobbie" value="Músics" />;
          <label for="Dança">Dança</label>
          <input type="checkbox" v-model="Hobbie" value="Dança" />;
          <label for="Artes">Artes</label>
          <input type="checkbox" v-model="Hobbie" value="Artes"/>;
          <label for="Outros">Outros...</label>
          <input type="checkbox" v-model="Hobbie" value="Outros"/>
        </div>
        <hr>
         <button>Linguagem de programação:</button>
         <input type="text" v-on:keypress="ok=false" v-model="linguagem" placeholder="Digite sua linguagem"  class="labelImput" />
         <hr>
         <p><button>Biografia:</button></p>
         <textarea v-model="texto" placeholder="Digite sua biografia"></textarea>
         <p style="white-space: pre-line;"></p>
         <hr>
       <label for="estado" >Estado:</label>
       <select v-on:keypress="ok=false" v-model="estado">
         <option value="AC">Acre</option>
         <option value="AL">Alagoas</option>
         <option value="AP">Amapá</option>
         <option value="AM">Amazonas</option>
         <option value="BA">Bahia</option>
         <option value="CE">Ceará</option>
         <option value="DF">Distrito Federal</option>size: 1000px;
         <option value="ES">Espírito Santo</option>
         <option value="GO">Goías</option>
         <option value="MA">Maranhão</option>
         <option value="MT">Mato Grosso</option>
         <option value="MS">Mato Grosso do Sul</option>
         <option value="MG">Minas Gerais</option>
         <option value="PA">Pará</option>
         <option value="PB">Paraíba</option>
         <option value="PE">Pernambuco</option>
         <option value="PI">Piauí</option>
         <option value="RJ">Rio de Janeiro</option>
         <option value="RN">Rio Grande do Norte</option>
         <option value="RS">Rio Grande do Sul</option>
         <option value="RO">Rondônia</option>
         <option value="RR">Roráima</option>
         <option value="SC">Santa Catarina</option>
         <option value="SP">São Paulo</option>
         <option value="SE">Sergipe</option>
         <option value="TO">Tocantins</option>
       </select>
       <hr>
       <input
          type="file"
          id="avatarField"
          @change="handleFileUpload($event)"/>
          <hr>
       <p><button @click="ok = !ok">Mostrar</button></p>
       <hr>
       </fieldset>
      </form>
    </div>
  </div>
  <div v-if="ok">
    <p>O seu nome é: {{ nome }}</p>
    <p>O seu email é: {{ email }}</p>
    <p>A sua senha é: {{ senha }}</p>
    <p>A sua confirmação de senha é: {{ confirma }}</p> 
    <p>A sua data de nascimento é: {{ data }}</p>
    <p>O seu endereço é: {{ endereco }}</p>
    <p>A sua cidade é: {{ cidade }}</p>
    <p>O seu estado é: {{ estado }}</p>
    <p>O seu hobbie é: {{ hobbie }}</p>
    <p>A sua linguagem de programação é: {{ linguagem }}</p>
    <p>A sua biografia é: {{ biografia }}</p>
  </div>
</template>
<style>
body{
  font-family: Arial, Helvetica, sans-serif;
  background-image: linear-gradient(to right, rgb(20,147,220), rgb(17,54,71));
}
.box{
  color: white;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: rgb(0, 0, 0, 0.8);
  padding: 15px;
  border-radius: 15px;
  width: 20%;
}
fieldset{
  border: 3px solid dodgerblue;
}
legend{
  border: 1px solid dodgerblue;
  padding: 10px;
  text-align: center;
  background-color: dodgerblue;
  border-radius: 8px;
  color: white;
}
input.box{
  position: relative;
}
.imputUser{
  background: none;
  border: none;
  border-bottom: 1px solid white;
  outline: none;
  font-size: 15px;
  width: 100%;
  letter-spacing: 2px;
}
.labelInput{
  position: absolute;
  top: 0px;
  left: 0px;
  pointer-events: none;
  transition: .5s;
}
</style>style="width: 200px"