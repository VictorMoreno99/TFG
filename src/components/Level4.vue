<template>
  <div id="Level 4">
    <div v-if="page === 0">
      <h1> Level 4 </h1>
      <h2> Admins </h2>
      <p>
        In this level we will talk about fake messages from the support team or the admins of some websites.
      </p>
      <img src="../assets/detectiua.png"
           alt="Fail"
           style="width: 200px"
      >
      <button v-on:click="setPage(1)"> Next Page </button>
    </div>
    <div v-if="page === 1">
      <h3> <i> Check out these emails </i> </h3>
        <img src="../assets/phishing1.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      <div style="font-size: 20px"> Email 1 </div>
      <button v-on:click="setPage(2)"> Next Page </button>
    </div>
    <div v-if="page === 2">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>

        <img src="../assets/phishing2.png" alt="" style="width: 300px; padding: 10px 0 10px 0">

      <div style="font-size: 20px"> Email 2 </div>
      <button v-on:click="setPage(3)"> Next Page </button>
    </div>
    <div v-if="page === 3">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>

        <img src="../assets/phishing3.png" alt="" style="width: 300px; padding: 10px 0 10px 0">

      <div style="font-size: 20px"> Email 3 </div>
      <button v-on:click="setPage(4)"> Next Page </button>
    </div>
    <div v-if="page === 4">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>

        <img src="../assets/phishing4.png" alt="" style="width: 300px; padding: 10px 0 10px 0">

      <div style="font-size: 20px"> Email 4 </div>
      <button v-on:click="setPage(5)"> Next Page </button>
    </div>
    <div v-if="page === 5">
      <h3> How many are not from real support? </h3>
      <button v-on:click="setPage(7)"> 1 Email</button>
      <button v-on:click="setPage(7)"> 2 Emails</button>
      <button v-on:click="setPage(7)"> 3 Emails</button>
      <button v-on:click="setPage(6)"> All of them</button>
    </div>
    <div v-if="page === 6">
      <h1> Eureka! </h1>
      <h2> Here you have some hints that might help you in the future </h2>
      <p> - Actual support will never ask for your password so check that out! </p>
      <p> - Companies do not use public domains, so if you see a strange domain go to a search engine and look for it! </p>
      <p> - If it includes suspicious links or attachments it probably is a scam so if you look at the URL and it seems suspicious don't click!</p>
      <button v-on:click="$emit('swapto', 'endgame')" > Got It! </button>
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
  name: "Level4",
  data: function (){
    return {
      page: 0,
    }
  },
  methods:{
    setPage(number){
      this.page = number;
      this.counter++;
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
