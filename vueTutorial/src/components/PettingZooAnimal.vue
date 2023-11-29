<template>
<img @click="state.timesPet++" :src="state.imageURL"/>
<p>Times the dangerous animal was pet: {{state.timesPet}}</p>
</template>

<script setup>
import {reactive, watch} from "vue";
const state = reactive({
  timesPet: 0,
  imageURL: "https://hacksu.com/animals/alpaca.jpg"
})

function maybewriting(){
  if(Math.random() < 0.1){
    state.imageURL = "https://hacksu.com/animals/alpaca-fire.gif"
  }
}

watch(state, maybewriting)
</script>