<template>
  <div id="Endgame">
    <h1> Congrats!</h1>
    <h2> Here it is a quick recap: </h2>
    <p> - Always look for followers/follows ratio and publications first! </p>
    <p> - Check if they are focused on promoting their low prices, not a good sign. </p>
    <p> - First check out the source and look for other articles about the same. If they don't have any competitor maybe the event is not that truthful! </p>
    <p> - Support will never ask for personal information and will contact you from their enterprise mail so check it out! </p>
    <h2> Remember all of these elements! </h2>
    <button v-on:click="$emit('swapto', 'PostQuestion')" > Got It! </button>
  </div>
</template>

<script>
export default {
  name: "Endgame"
}
</script>

<style scoped>
h1{
  font-size: 40px;
}
h2{
  padding-top: 10px;
  line-height: 25px;
}
h3{
  color:white;
  font-size: 25px;
  padding-bottom: 10px;
}



</style>
