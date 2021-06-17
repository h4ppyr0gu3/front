<template>
	<nav class="navbar" style="background-color: black;">
  <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <p class="is-size-4 has-text-white">musicApp</p>
    </a>

    <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample" v-on:click="handleBurger">
      <span aria-hidden="true" class="has-text-white"></span>
      <span aria-hidden="true" class="has-text-white"></span>
      <span aria-hidden="true" class="has-text-white"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
      <a class="navbar-item">
        Home
      </a>

      <a class="navbar-item">
        Documentation
      </a>

      <div class="navbar-item has-dropdown is-hoverable">
        <a class="navbar-link">
          More
        </a>

        <div class="navbar-dropdown">
          <a class="navbar-item">
            About
          </a>
          <a class="navbar-item">
            Jobs
          </a>
          <a class="navbar-item">
            Contact
          </a>
          <hr class="navbar-divider">
          <a class="navbar-item">
            Report an issue
          </a>
        </div>
      </div>
    </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a class="button is-primary">
            <strong>Sign up</strong>
          </a>
          <a class="button is-light">
            Log in
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>

</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String
  }, 
  methods:{
	handleBurger() {
		console.log("something")
	}
  }
}
</script>

<style scoped>


</style>