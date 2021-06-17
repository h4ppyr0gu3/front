<template>
  <Header v-if="page == 'home' " msg="Welcome to Your Vue.js App"/>
  <Landing v-if="page == 'landing'" @handleClick="page = $event"/>
  <Login v-if="page == 'login'"/>
  <Signup v-if="page == 'signup'"/>
</template>

<script>
import Header from './components/header.vue'
import Landing from './components/static_pages/Landing.vue'
import Login from './components/static_pages/Login.vue'
import Signup from './components/static_pages/Signup.vue'

export default {
  name: 'App',
  components: {
    Header,
    Login,
    Landing,
    Signup
  },
  data: function() {
    return {
      page: "landing"
    }
  },
  methods: {
    click: function(){
      console.log("clicked")
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  width: 100%;
  height: 100%;
}
</style>
