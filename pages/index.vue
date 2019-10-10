<template>
  <div>
    <nav class="header-nav">
      <ul class="nav-list">
        <li class="nav-list-item">
          <a href="#" class="nav-link">Home</a>
        </li>
        <li class="nav-list-item">
          <a href="#" class="nav-link">About</a>
        </li>
        <li class="nav-list-item">
          <a href="#" class="nav-link">Contact</a>
        </li>
      </ul>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
        <a href="https://github.com/nuxt/nuxt.js" target="_blank" class="button--grey">GitHub</a>
      </div>
    </nav>
    <div class="container">
      <logo class="logo" />
      <h1 class="title">concatconf-exercise</h1>
      <h2 class="subtitle">My flawless Nuxt.js project</h2>
      <div class="form-wrapper">
        <h2 class="register">Register</h2>
        <form action="#">
          <label for="first-name">First Name</label>
          <input type="text" v-model="firstName" placeholder="Your first name" />

          <label for="last-name">Last Name</label>
          <input type="text" v-model="lastName" placeholder="Your last name" />

          <input type="submit" value="Submit" v-on:click="submit" />
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  },
  data: () => ({
    firstName: "",
    lastName: ""
  }),
  methods: {
    submit: function() {
      console.log(this.firstName, this.lastName);

      this.firstName = "";
      this.lastName = "";
    }
  }
};
</script>

<style>
.container {
  margin: 70px auto;
  min-height: 100vh;
  display: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}


.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.header-nav {
  width: 100%;
  display: flex;
  justify-content: space-between;
  box-shadow: 2px 1px 0px 2px #000;
}

.nav-list {
  list-style: none;
  padding: 0;
  display: flex;
  justify-content: center;
}

.nav-list-item {
  margin: 0 1em;
}

.nav-link {
  text-decoration: none;
}

.nav-link:hover {
  color: green;
}
form {
  margin: auto;
  width: 70%;
  text-align: left;
}

.form-wrapper {
  height: 100%;
  display: flex;
  flex-direction: column;
}

input[type="text"] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
  border: 1px solid green;
  border-radius: 12px;
  outline: none;
}

input[type="submit"] {
  width: 100%;
  background-color: #4caf50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 12px;
  cursor: pointer;
}

input[type="submit"]:hover {
  background-color: #45a049;
}

input[type="submit"]:hover {
  background-color: #45a049;
}
</style>
