<template>
  <div id="PreQuestion">
    <h1> STOP! </h1>
    <p>
      Before you start! <br> Complete this questionnaire and then start the game for the complete experience!
      <br><br>
      If you have any questions don't hesitate and ask them!
    </p>
    <a href="https://docs.google.com/forms/d/e/1FAIpQLSfxHuYfQ-GOQrizgxOl7eGPeWh8vPFl9xz578Q94AE_xNPJmA/viewform?usp=sf_link" style="text-decoration: unset">
      <button>
        Questionnaire
      </button>
    </a>
    <button v-on:click="$emit('swapto', 'Login')">
      Next
    </button>
  </div>
</template>

<script>
export default {
  name: "PreQuestion"
}
</script>

<style scoped>

</style>
