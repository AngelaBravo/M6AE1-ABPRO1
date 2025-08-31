<script setup>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
import Head from './components/Head.vue';
import Formulario from './components/Formulario.vue';
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/Favicon3.jpg" height="125" />
    <div class="wrapper">
      <Head msg="M6AE1-ABPRO1" />
    </div>
  </header>

  <main>
    <!-- <TheWelcome /> -->
     <Formulario />
  </main>
</template>


<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
