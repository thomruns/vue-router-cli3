<template>
  <nav id="main-nav">
    <router-link :to="{ name: 'Home'}">Home</router-link> |
    <router-link :to="{ name: 'About'}">About</router-link> |
    <router-link :to="{ name: 'Contact' }">Contact</router-link> |
    <p>User Profiles</p>
    <ul id="users">
      <li v-for="(id, index) in userIds" :key="index">
        <router-link :to="{ name: 'ViewProfile', params: { user_id: id} }">User{{id}}</router-link>
      </li>
    </ul>
    <h2>Navigation Controls</h2>
    <ul class="nav-controls">
      <li><button @click="goBack">&lt;&lt; Go Back</button></li>
      <li><button @click="goHome">Redirect to Home</button></li>
      <li><button @click="goForward">Go Forward &gt;&gt;</button></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      userIds: ['1', '2','3','4','5']
    }
  },
  methods: {
    goHome() {
      this.$router.push({ name: 'Home' })
    },
    goBack() {
      this.$router.go(-1)
    },
    goForward() {
      this.$router.go(1)
    }
  }
}
</script>

<style>
a {
  text-decoration: none;
}
#main-nav {
  padding: 20px;
  background: #5a97a3;
  margin: 5px;
  border: 1px solid #fff;
}

#main-nav a {
  font-weight: bold;
  color: #265683;
}

#main-nav a.router-link-exact-active {
  color: #125235;
}
#users li {
  list-style: none;
  display: inline-block;
  padding: 10px;
}
#users a.router-link-exact-active {
  color: #668822;
}
.nav-controls li{
  display: inline-block;
  list-style: none;
}
button {
  padding: 10px;
  margin: 5px;
  border-radius: 5px;
  font-size: 1.2em;
  color: #265683;
  outline: none;
}
</style>
