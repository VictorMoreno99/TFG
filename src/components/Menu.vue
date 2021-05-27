<template>
  <div id="Menu">
    <h2> Hi {{this.name}}! </h2>
    <h3> Select a level </h3>
    <button v-on:click="$emit('swapto', 'Level1')" > Level 1 </button>
    <button v-on:click="$emit( 'swapto', 'Level2')"> Level 2 </button>
    <button v-on:click="$emit( 'swapto', 'Level3')"> Level 3 </button>
    <button v-on:click="$emit('swapto', 'Level4')"> Level 4 </button>
  </div>
</template>

<script>
export default {
  name: "Menu",
  props: ['name']
}

</script>

<style scoped>

</style>
