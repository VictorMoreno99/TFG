<template>
  <div id="Level 2">
    <div v-if="page === 0">
      <h1> Level 2 </h1>
      <h2> Shops </h2>
      <p>
        In this level we will dive into shops and check if they are truly real and sell original products or
        they are fake or dropshipping shops.
      </p>
      <img src="../assets/detectiua.png"
           alt="Fail"
           style="width: 200px"
      >
      <button v-on:click="setPage(1)"> Next Page </button>
    </div>
    <div v-if="page === 1">
      <h3> <i> Check these shops </i> </h3>
      <a href="https://www.zara.com/es/ca/">
        <img src="../assets/logozara.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      </a>
      <div style="font-size: 20px"> Shop 1 </div>
      <button v-on:click="setPage(2)"> Next Page </button>
    </div>
    <div v-if="page === 2">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>
      <a href="https://es.shein.com">
        <img src="../assets/shein-logo.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      </a>
      <div style="font-size: 20px"> Shop 2 </div>
      <button v-on:click="setPage(3)"> Next Page </button>
    </div>
    <div v-if="page === 3">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>
      <a href="https://www.asos.com">
        <img src="../assets/asoslogo.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      </a>
      <div style="font-size: 20px"> Shop 3 </div>
      <button v-on:click="setPage(4)"> Next Page </button>
    </div>
    <div v-if="page === 4">
      <h3 style="color:white;font-size: 25px"> <i> Look at these profiles </i> </h3>
      <a href="https://www.fashiontiy.com">
        <img src="../assets/flogo.png" alt="" style="width: 300px; padding: 10px 0 10px 0">
      </a>
      <div style="font-size: 20px"> Shop 4 </div>
      <button v-on:click="setPage(5)"> Next Page </button>
    </div>
    <div v-if="page === 5">
      <h3> How many provide <br> non-original content? </h3>
      <button v-on:click="setPage(8)"> 1 Shop</button>
      <button v-on:click="setPage(7)"> 2 Shops</button>
      <button v-on:click="setPage(7)"> 3 Shops</button>
      <button v-on:click="setPage(7)"> All of them</button>
    </div>
    <div v-if="page === 6">
      <h1> Eureka! </h1>
      <h2> Here you have some hints that might help you in the future </h2>
      <p> - A product is advertised at an unbelievably low price, or advertised to have amazing benefits or features that sound too good to be true.. </p>
      <p> - The social media based store is very new and selling products at very low prices. The store may have limited information about delivery and other policies. </p>
      <p> - The other party insists on immediate payment, or payment by electronic funds transfer or a wire service.</p>
      <button v-on:click="$emit('swapto', 'Level3')" > Got It! </button>
    </div>
    <div v-if="page === 7">
      <h1> TRY AGAIN! </h1>
      <img src="../assets/x.png" alt="" style="width: 250px; padding: 20px 0 20px 0">
      <button v-on:click="setPage(1)"> Go Back </button>
    </div>
    <div v-if="page === 8">
      <h3> Which one?</h3>
      <button v-on:click="setPage(7)"> ZARA</button>
      <button v-on:click="setPage(7)"> SHEIN</button>
      <button v-on:click="setPage(7)"> ASOS</button>
      <button v-on:click="setPage(6)"> FashionTY</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Level2",
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
