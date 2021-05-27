<template>
  <div id="Start">
    <p>MY GAME</p>
    <button v-on:click="$emit('swapto', 'Login')">
      New Game
    </button>
    <button>
      Help
    </button>
  </div>
</template>

<script>
export default {
  name: "Start"
}
</script>

<style scoped>

</style>
