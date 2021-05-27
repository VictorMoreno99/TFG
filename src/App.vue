<template>
  <div id="app">
    <keep-alive>
      <component v-bind:is="stage" v-on:swapto="setStage($event)"
                 v-on:getname="savename($event)"
                 v-bind:name="username" ></component>
    </keep-alive>
  </div>
</template>

<script>
import Level1 from './components/Level1.vue'
import Level2 from './components/Level2.vue'
import Level3 from './components/Level3.vue'
import Level4 from './components/Level4.vue'
import Menu from './components/Menu.vue'
import Endgame from './components/Endgame.vue'
import Start from './components/Start.vue'
import Login from './components/Login.vue'

export default {
  name: 'App',
  data: function(){
    return {
      stage: 'Start',
      username: '',
    };
  },
  components: {
    Level1,
    Level2,
    Level3,
    Level4,
    Menu,
    Endgame,
    Start,
    Login
  },
  methods:{
    setStage: function (v) {
      this.stage = v;
    },
    savename: function (name){
      this.username = name;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
