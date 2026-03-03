<script setup>
    /* Aula 2 v-model
    import { ref } from 'vue'
    const mostrar = ref(false)
    const texto = ref('')
    */
    import { ref } from 'vue';
    const contador = ref(0);
    function incrementar(number) {
      if(!Number.isNaN(number)) {
        contador.value += number;
      }
      if(contador.value >= 10) {
        contador.value = 10;
      }
    }
    function decrementar(number) {
      if(!Number.isNaN(number)) {
        contador.value -= number;
      }
      if(contador.value <= 0) {
        contador.value = 0;
      }
    }
</script>

<template>
  <main>
    <label>Valor a incrementar/decrementar: </label>
    <h1>{{ contador }}</h1>
  <input type="number" v-model="number" min="1" max="10" value="1">
  <div>
      <button :disabled="contador <= 0" @click="decrementar(Number(number))">Decrementar</button>
      <button :disabled="contador >= 10" @click="incrementar(Number(number))">Incrementar</button>
    </div>
  </main>
   <!-- Aula 2 v-model
    <div>
        <input type="text" v-model="texto">
        <label>{{ texto }}</label>
        <button @click="mostrar = !mostrar">Mostrar/Ocultar</button>
        <div v-if="mostrar">
            <p>Conteúdo exibido.</p>
        </div>
        <div v-else>
            <p>Conteúdo ocultado.</p>
        </div>
    </div>
    -->

</template>

<style scoped>

</style>
