<template>
  <Dashboard v-if="page == 'dashboard'" @handleClick="page = $event"/>
  <Landing v-if="page == 'landing'" @handleClick="page = $event"/>
  <Login v-if="page == 'login'" @handleClick="page = $event"/>
  <Signup v-if="page == 'signup'" @handleClick="page = $event"/>
</template>

<script>
import Landing from './components/static_pages/Landing.vue'
import Login from './components/static_pages/Login.vue'
import Signup from './components/static_pages/Signup.vue'
import Dashboard from './components/static_pages/Dashboard.vue'

export default {
  name: 'App',
  components: {
    Login,
    Dashboard,
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
  font-family: 'Montserrat', sans-serif;
  width: 100%;
  height: 100%;
}
</style>
