<script setup lang="ts">

  import HelloWorld from './components/HelloWorld.vue'
  import TheWelcome from './components/TheWelcome.vue'
  import { defineComponent, ref, computed, onMounted } from 'vue';

  let test = ref("hello")

  onMounted(() => {
    doSomething(test.value)
  })

</script>

<template>

  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
    <div class="wrapper">
      <HelloWorld msg="Let's cron!" />
    </div>
  </header>

  <main>
    <h1 :value="HelloWorld.cronExpressionInput"></h1>
    <TheWelcome />
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


<script lang="ts">

  export default defineComponent({
    name: 'TestComp',
  })

  function doSomething (param : any) {
    console.log(param);
  }
  
  
</script>