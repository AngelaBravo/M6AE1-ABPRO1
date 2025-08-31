<template>
    <form>
        <input v-model="nombre" type="text" class="form-control mb-3" placeholder="Nombre">
        <!-- <P>Tu nombre es: {{ nombre }}</P> -->

        <div class="mb-3">
            <!-- <label for="exampleInputEmail1" class="form-label">Email address</label> -->
            <input v-model="email" type="email" class="form-control" id="exampleInputEmail1" placeholder="E-mail">
            <!-- <div id="emailHelp" class="form-text">Tu email es: {{ email }}</div> -->
        </div>
        <input v-model="edad" type="text" class="form-control mb-3" placeholder="Edad">
        <!-- <P>Tu edad es: {{ edad }}</P> -->
        <button type="submit" class="btn btn-primary">Submit</button>

        <h3 class="mt-4" >Resumen</h3>
        <p>Nombre: {{ nombre }}</p>
        <p>Email: {{ email }}</p>
        <p>Edad: {{ edad }}</p>

    </form>
</template>

<script setup>
import { ref } from 'vue';

const nombre = ref('');
const email = ref('');
const edad = ref('');
</script>
