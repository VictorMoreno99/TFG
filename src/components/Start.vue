<template>
  <div id="Start" class="styling">
    <h1>Fraud or not?</h1>
    <p>
      Hi! Welcome to Fraud or Not, the game where you decide everything! <br> <br>
      Follow the instructions and read carefully to get the most out of the game!
      <br><br>
      If you have any questions don't hesitate and ask them!
    </p>
    <button v-on:click="$emit('swapto', 'PreQuestion')">
      PLAY
    </button>
    <img src="../assets/gl2.png" alt="" style="width: 150px; padding-top: 20px">
  </div>
</template>

<script>
export default {
  name: "Start"
}
</script>

<style>
body{
  background: #e1eec3;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #f05053, #e1eec3);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #f05053, #e1eec3); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  height: 100vh;
  display: block;
  justify-content: center;
  padding: 30px 30px 0px 30px;
  line-height: 22px;
}
h1{
  color: white;
  font-family: Arial;
  font-size: 45px;
}
p{
  padding-top: 10px;
  color: white;
  text-align: justify;
}
button{
  display: block;
  margin: 0 auto;
  margin-top: 20px;
  box-sizing: border-box;
  border: 1px solid transparent;
  border-radius: 8px;
  background-color: black;
  color: white;
  font-family: Arial;
  font-weight: bold;
  font-size: 20px;
  padding: 10px;
}
h2{
  line-height: 28px;
}


</style>
