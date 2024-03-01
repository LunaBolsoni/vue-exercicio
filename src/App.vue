<script setup>
import { ref } from 'vue'
const contador = ref(0)
function incrementar() {
  contador.value++;
}
function decrementar() {
  if (contador.value > 0) {
    contador.value--;
  }
}
function reiniciar() {
  contador.value = 0
}
</script>
<template>
  <button @click="incrementar">+</button>
  <button @click="decrementar">-</button>
  <button @click="reiniciar">zerar</button>
  <p>Valor do contador: {{ contador }}</p>
</template>
<style scoped>
button {
  background-color: black;
  color: aliceblue;
  margin: 5pxe;
  padding: 20px;
  width: 100px;
}
</style>  