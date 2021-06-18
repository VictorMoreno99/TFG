<template>
  <div id="Level 1">
    <div v-if="page === 0">
      <h1> Level 1</h1>
      <h2> Profiles </h2>
      <p>
        In this level we will take a close look at the authenticity of some profiles and
        how they can be detected so be aware of them so you don't miss any detail!!
      </p>
      <img src="../assets/detectiua.png"
           alt="Fail"
           style="width: 200px"
      >
      <button v-on:click="setPage(1)"> Next Page </button>
    </div>
    <div v-if="page === 1">
      <h3> <i> Look at these profiles </i> </h3>
      <img src="../assets/prof1.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      <div style="font-size: 20px"> Profile 1 </div>
    <button v-on:click="setPage(2)"> Next Page </button>
    </div>
    <div v-if="page === 2">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>
      <img src="../assets/prof2.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      <div style="font-size: 20px"> Profile 2 </div>
      <button v-on:click="setPage(3)"> Next Page </button>
    </div>
    <div v-if="page === 3">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>
      <img src="../assets/prof3.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      <div style="font-size: 20px"> Profile 3 </div>
      <button v-on:click="setPage(4)"> Next Page </button>
    </div>
    <div v-if="page === 4">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>
      <img src="../assets/prof4.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      <div style="font-size: 20px"> Profile 4 </div>
      <button v-on:click="setPage(5)"> Next Page </button>
    </div>
    <div v-if="page === 5">
      <h3> How many are fake? </h3>
      <button v-on:click="setPage(7)"> 1 profile</button>
      <button v-on:click="setPage(7)"> 2 profiles</button>
      <button v-on:click="setPage(7)"> 3 profiles</button>
      <button v-on:click="setPage(6)"> All of them</button>
    </div>
    <div v-if="page === 6">
      <h1> Eureka! </h1>
      <h2> Here you have some hints that might help you in the future </h2>
      <p> - Look if the followers/follows ratio is balanced. </p>
      <p> - Check when the account was created. Newer accounts tend to be fake! </p>
      <p> - Look at how many publications does it have. If the account uploaded them all in short time
      it might be fake!</p>
      <button v-on:click="$emit('swapto', 'Level2')" > Got It! </button>
    </div>
    <div v-if="page === 7">
      <h1> TRY AGAIN! </h1>
      <img src="../assets/x.png" alt="" style="width: 250px; padding: 20px 0 20px 0">
      <button v-on:click="setPage(1)"> Go Back </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Level1",
  data: function (){
    return {
      page: 0,
    }
  },
  methods:{
    setPage(number){
      this.page = number;
    },
  }
}
</script>

<style scoped>
h1{
  font-size: 40px;
}
h2{
  padding-top: 10px;
}
h3{
  color:white;
  font-size: 25px;
  padding-bottom: 10px;
}

</style>
