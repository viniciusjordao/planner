<script setup>
import { ref } from 'vue'
const props = defineProps({
  user: Object
})

const open = ref(false)

const  { user } = props

const caloriasTotais =  
    user.macronutrientes.carbo +
    user.macronutrientes.prot +
    user.macronutrientes.doce +
    user.macronutrientes.graos 


  

</script>

<template>
  <li class="card">
    <img/>
    <div>{{ user.name }}</div>
    <div>Calorias Totais: {{caloriasTotais}}</div>
    <div @click="open = true">Plano Alimentar</div>
    </li>
    <div v-if="open" class="modal-content">
    <p>Carboidratos: {{user.macronutrientes.carbo}}</p>
    <p>Proteínas: {{user.macronutrientes.prot}}</p>
    <p>Doces: {{user.macronutrientes.doce}}</p>
    <p>Graos: {{user.macronutrientes.graos}}</p>
    <h3>{{ caloriasTotais }}</h3>
    <button @click="open = false">Close</button>
  </div>
  <div v-if="open" class="modal"></div>
</template>

<style scoped>
.card{
 list-style: none ;
 padding: 20px 44px;
}

.card img{
  width: 150px;
  height: 200px;
  background-color: blueviolet;
}

.modal {
  position: fixed; /* Stay in place */
  z-index: 888; /* Sit on top */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.6); /* Black w/ opacity */
}

.modal-content {
  position: fixed;
  z-index: 999;
  top: 20%;
  left: 50%;
  width: 300px;
  margin-left: -150px;
  background-color: aliceblue;
  padding: 20px;
  color: black;
}

</style>