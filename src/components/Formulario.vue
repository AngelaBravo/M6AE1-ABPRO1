<template>
    <form @submit.prevent="resetearSubmit">
        <p>Por favor completa todos los datos {{ nombre }}</p>
        <input v-model="nombre" type="text" class="form-control mb-3" placeholder="Nombre">
        <input v-model="email" type="email" class="form-control mb-3" id="exampleInputEl1" placeholder="E-mail">
        <input v-model="edad" type="text" class="form-control mb-3" placeholder="Edad">
        <button type="submit" class="btn btn-primary" v-on:click="mostrarResumenFormulario">Submit</button>
        <button type="button" class="btn btn-outline-dark mx-5" @click="resetearFormulario">Limpiar Información</button>

        <slot name="resumen" v-if="mostrarResumen">
            <h3 class="mt-4">Resumen</h3>
            <p>Nombre: {{ nombreResumen }}</p>
            <p>Email: {{ emailResumen }}</p>
            <p>Edad: {{ edadResumen }}</p>
        </slot>

    </form>
</template>

<script setup>
import { ref } from 'vue';

const nombre = ref('');
const email = ref('');
const edad = ref('');
const mostrarResumen = ref(false);

const nombreResumen = ref('');
const emailResumen = ref('');
const edadResumen = ref('');

function mostrarResumenFormulario() {
    nombreResumen.value = nombre.value;
    emailResumen.value = email.value;
    edadResumen.value = edad.value;
    mostrarResumen.value = true;
    nombre.value = '';
    email.value = '';
    edad.value = '';
}

function resetearFormulario() {
    mostrarResumen.value = false; // aquí se podría ocupar el v-else?
}
</script>
