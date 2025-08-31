<template>
    <form>
        <input v-model="nombre" type="text" class="form-control mb-3" placeholder="Nombre">
        <input v-model="email" type="email" class="form-control mb-3" id="exampleInputEl1" placeholder="E-mail">
        <input v-model="edad" type="text" class="form-control mb-3" placeholder="Edad">
        <button type="submit" class="btn btn-primary">Submit</button>
        
        <slot name="resumen">
            <h3 class="mt-4" >Resumen</h3>
            <p>Nombre: {{ nombre }}</p>
            <p>Email: {{ email }}</p>
            <p>Edad: {{ edad }}</p>
        </slot>

    </form>
</template>

<script setup>
import { ref } from 'vue';

const nombre = ref('');
const email = ref('');
const edad = ref('');
</script>
