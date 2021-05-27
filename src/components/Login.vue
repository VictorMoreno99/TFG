<template>
  <div id="Login">
    <input type="text" placeholder="Write your name here" v-model="fname">
    <button v-on:click="$emit('swapto', 'Menu')"
            v-on:mouseover="$emit('getname', fname)"

    > Save </button>
  </div>
</template>

<script>
export default {
  name: "Login",
  data: function (){
    return {
      fname: '',
    }
  }
}
</script>

<style scoped>

</style>
