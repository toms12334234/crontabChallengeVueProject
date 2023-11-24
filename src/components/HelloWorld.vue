

<template>
  <div class="greetings">
    <h1 class="green">{{ who }}</h1>
    
    <div>
      <h2>
        <label for="jack">Cron expression:</label>
        <input id="jack" :value="cronExpressionInput">
        <br />
      </h2>
    </div>

    <div>
      <h2>
        <label for="explanation">Cron explained:</label>
        <input id="explanation" disabled="true" value="Every minute">
      </h2>
    </div>

    <table>
      <tr>
        <th>Symbol</th>
        <th>Meaning</th>
      </tr>
      <tr>
        <td>*</td>
        <td>any value</td>
      </tr>
      <tr>
        <td>,</td>
        <td>list separator</td>
      </tr>
      <tr>
        <td>-</td>
        <td>range separator</td>
      </tr>
      <tr>
        <td>/</td>
        <td>step values</td>
      </tr>
    </table>

  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      who: "DATA",
      cronExpressionInput: "",
      
    };
  },
};
</script>

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

input {
  font-size: 24px;
}
</style>
