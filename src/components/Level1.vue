<template>
  <div id="Level 1">
    <div> Level 1: Profiles </div>
    <div v-if="page === 1">
      <div> Choose the fake profile </div>
      <img :src="require('C:\\Users\\usuario\\Documents\\GitHub\\tfg-test\\src\\assets\\logo.png')"/>
      <div> Profile 1 </div>
      <img
        :src="require('C:\\Users\\usuario\\Documents\\GitHub\\tfg-test\\src\\assets\\logo.png')"
    />
    <div> Profile 2 </div>
    <button v-on:click="setPage(2)"> Next Page </button>
    </div>
    <div v-if="page === 2">
      <div> Choose the fake profile </div>
      <img :src="require('C:\\Users\\usuario\\Documents\\GitHub\\tfg-test\\src\\assets\\logo.png')"/>
      <div> Profile 3 </div>
      <img
          :src="require('C:\\Users\\usuario\\Documents\\GitHub\\tfg-test\\src\\assets\\logo.png')"
      />
      <div> Profile 4 </div>
      <button v-on:click="setPage(3)"> Next Page </button>
    </div>
    <div v-if="page === 3">
      <text class="text-color-primary"> Which one is fake?</text>
      <button v-on:click="setPage(4)"> Image 1 </button>
      <button v-on:click="setalert()"> Image 2 </button>
      <button v-on:click="setalert()"> Image 3 </button>
      <button v-on:click="setalert()"> Image 4 </button>
    </div>
    <div v-if="page === 4">
      <div> Hints </div>
      <div> - Try to look at the followers </div>
      <div> - In twitter try look for when the account was created </div>
      <div> - Look for patterns in photos, if they look similar,
        be careful!</div>
      <button v-on:click="$emit('swapto', 'Level2')" > Got It! </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Level1",
  data: function (){
    return {
      page: 1,
    }
  },
  methods:{
    setPage(number){
      this.page = number;
    },
    setalert() {
      alert('You are wrong!');
    }
  }
}
</script>

<style scoped>


</style>
