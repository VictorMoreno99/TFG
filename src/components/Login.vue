<template>
  <div id="Login">
    <h1> Who are you? </h1>
    <h2>Choose your name:</h2>
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
h1{
  font-size: 40px;
}

</style>
