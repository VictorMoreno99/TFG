<template>
  <div id="Level 3">
    <div v-if="page === 0">
      <h1> Level 3 </h1>
      <h2> News </h2>
      <p>
        Are you not sure that what you read is trusted? Check out this level and learn some things that may help you!
      </p>
      <img src="../assets/detectiua.png"
           alt="Fail"
           style="width: 200px"
      >
      <button v-on:click="setPage(1)"> Next Page </button>
    </div>
    <div v-if="page === 1">
      <h3> <i> Review these news </i> </h3>
      <a href="https://zapatopi.net/treeoctopus/">
        <img src="../assets/pulpo.png" alt="" style="width: 300px; padding: 10px 0 10px 0; height: 400px">
      </a>
      <div style="font-size: 20px"> Save the endangered tree octopus! </div>
      <button v-on:click="setPage(2)"> Next Page </button>
    </div>
    <div v-if="page === 2">
      <h3 style="color:white;font-size: 25px"> <i> Review these news </i> </h3>
      <a href="https://worldnewsdailyreport.com/florida-teenager-lying-in-critical-condition-after-inserting-his-genitals-inside-of-a-blowfish/">
        <img src="../assets/fish.jpg" alt="" style="width: 300px; padding: 10px 0 10px 0">
      </a>
      <div style="font-size: 20px"> A kid inserts its genitals on a blowfish! </div>
      <button v-on:click="setPage(5)"> Next Page </button>
    </div>
    <div v-if="page === 5">
      <h3> Which articles are fake? </h3>
      <button v-on:click="setPage(7)"> The kid</button>
      <button v-on:click="setPage(7)"> The octopus</button>
      <button v-on:click="setPage(6)"> Both</button>
      <button v-on:click="setPage(7)"> Neither</button>
    </div>
    <div v-if="page === 6">
      <h1> Eureka! </h1>
      <h2> Here you have some hints that might help you in the future </h2>
      <p> - First always check out the font of the article, including the reporter and the organization. In this case both were satirical websites with the intention of joking :P. </p>
      <p> - Check if other sources have covered the same event. If not you have a great clue that maybe the story is not that truth at all!</p>
      <p> - LOOK OUT FOR THE PHOTOS! Usually fake news use photoshopped photos and you can spot them if u look carefully or if you use tools as Google Reverse to check.</p>
      <button v-on:click="$emit('swapto', 'Level4')" > Got It! </button>
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
  name: "Level3",
  data: function (){
    return {
      page: 0,
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

h1{
  font-size: 40px;
}
h2{
  padding-top: 10px;
  line-height: 28px;
}
h3{
  color:white;
  font-size: 25px;
  padding-bottom: 10px;
}

</style>
