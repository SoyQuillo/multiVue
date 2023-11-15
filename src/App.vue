<script setup>

import { ref } from 'vue'

let numberEnter = ref(0);

let aux = ref(0);

function doClick(){

aux.value = numberEnter.value

}

</script>

<template>

<div>
 <input v-model="numberEnter"  type="number">
 <button @click="doClick">PRESIONAR</button>
 <h1>{{ numberEnter }}</h1>

 <h1 v-for="i in 10" :key="i" >
{{ aux * i }}
</h1>
</div>
  
</template>

<style scoped>

</style>
