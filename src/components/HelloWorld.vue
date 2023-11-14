<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <div>
      
      <h2>
        
        <label for="jack">Cron expression:</label>
        <input id="jack" value="Jack">
        <br />
      </h2>
        
      </div>
      <div>
        <h2>
          <label for="explanation">Cron explained:</label>
          <input id="explanation" disabled="true" value="Every minute">

        </h2>
      </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}

input
{
font-size:24px;
}

</style>
