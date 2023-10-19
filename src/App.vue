<script setup>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
import Exercise201 from './components/Exercise2-01.vue'
import Exercise202 from './components/Exercise2-02.vue';
import Practise201 from './components/Practise2-01.vue';
import Practise202 from './components/Practise2-02.vue';
import Practise203 from './components/Practise2-03.vue';
import Exercise203 from './components/Exercise2-03.vue';
import Exercise204 from './components/Exercise2.04.vue';
import Exercise205 from './components/Exercise2-05.vue'
import Practise205 from './components/Practise2-05.vue';
import Exercise206 from './components/Exercise2-06.vue';


</script>

<template>
  <header>
    <Practise201 class="styles" />
    <Exercise201 />
    <Practise202 />
    <Exercise202 />
    <Exercise203 />
    <Practise203 />
    <Exercise204 />
    <Exercise205 />
    <Practise205 />
    <Exercise206 />

  </header>

  <main>
    <!-- <TheWelcome /> -->
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
    flex-direction: column;
    /* place-items: center; */
    /* padding-right: calc(var(--section-gap) / 2); */
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .styles {
    margin-bottom: 20px;
  }
}
</style>
