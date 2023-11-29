<template>

  <template v-if="!state.saidhi">
  <h1>Story Ideas</h1>
  <h2>By {{fname}} {{lname}}</h2>
  <ul>
    <li>Bio World</li>
    <li>Geo World</li>
    <li>Ritual World</li>
    <li>{{idea}}</li>
  </ul>
  <button @click="state.saidhi=!state.saidhi">Say Hi?</button>
  <p v-if="state.saidhi">Thanks!</p>
  </template>

  <template v-else>
    <h2>WELCOME TO THE JUNGLE!</h2>
    <button @click="state.saidhi=!state.saidhi">Note stories?</button>
    <PettingZooAnimal/>
    <PettingZooAnimal/>
  </template>

</template>

<script setup>

// JavaScript for interactive content goes here
const fname = "Rowan";
const lname = "Ess";
//const idea = prompt("What is your idea")
import {reactive} from "vue";
const state = reactive({
  saidhi: false
});
import PettingZooAnimal from "./PettingZooAnimal.vue"

</script>

<style scoped>
h1 {
  color:navy;
}
* {
  font-family: sans-serif;
}
</style>
