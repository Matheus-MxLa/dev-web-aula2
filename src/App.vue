<script setup>
    /* Aula 2 v-model
    import { ref } from 'vue'
    const mostrar = ref(false)
    const texto = ref('')
    */
    import { ref } from 'vue'
    const number = ref('')
    const contador = ref(0)

    function incrementar() {
            contador.value++
    }
    function decrementar() {
        contador.value--
    }
</script>

<template>
    <button :disabled="contador <= 0" @click="decrementar">Decrementar</button>
    <button :disabled="contador >= 10" @click="incrementar">Incrementar</button>
    <p>{{ contador }}</p>
    <div>
        <input type="number" v-model="number">
        <label>{{ number }}</label>
    </div>

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
