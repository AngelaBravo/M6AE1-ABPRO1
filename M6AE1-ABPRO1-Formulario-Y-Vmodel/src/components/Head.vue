<template>
    <div class="greetings">
        <h1 class="green">{{ msg }}</h1>
        <h3>
            Llenemos el formulario con tus datos
        </h3>
    </div>
</template>

<script setup>
defineProps({
    msg: {
        type: String,
        required: true,
    },
})

</script>
<style>
.greetings {
    text-align: center;
    margin-bottom: 2rem;
}

.green {
    color: green;
}

@media (min-width: 1024px) {

    .greetings h1,
    .greetings h3 {
        text-align: left;
    }
}
</style>