<script setup>
import { ref } from 'vue'
import UserCard from './components/UserCard.vue'

const users = ref([
  {
    id: 0,
    name: "Felipe Lorem",
    macronutrientes: {
      carbo: 3000,
      prot: 2400,
      doce: 1000,
      graos: 1330
    }
  },
  {
    id: 1,
    name: "Renato Bonache",
    macronutrientes: {
      carbo: 3000,
      prot: 2000,
      doce: 5990,
      graos: 1000
    }
  },
  {
    id: 2,
    name: "Rosana Strinds",
    macronutrientes: {
      carbo: 3000,
      prot: 4000,
      doce: 6000,
      graos: 1000
    }
  },
  {
    id: 2,
    name: "Rosana Strinds",
    macronutrientes: {
      carbo: 3000,
      prot: 4000,
      doce: 6000,
      graos: 1000
    }
  },
  {
    id: 2,
    name: "Rosana Strinds",
    macronutrientes: {
      carbo: 3000,
      prot: 4000,
      doce: 6000,
      graos: 1000
    }
  },
  {
    id: 2,
    name: "Rosana Strinds",
    macronutrientes: {
      carbo: 3000,
      prot: 4000,
      doce: 6000,
      graos: 1000
    }
  }
])

localStorage.users = users

</script>

<template>

    <div class="container">
      <UserCard  v-for="user in users" :user="user" :key="user.id" />
    </div>

</template>

<style scoped>
.container{
  display: flex;
  flex-wrap: wrap;
}
@media (min-width: 1024px) {

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
