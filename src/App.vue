<template>
  <div id="app">
    <p>App.vue Instance</p>
    <Navbar />
    <router-view/>
    <Hello msg="Hello.vue Component in App.vue called outside the router-view"/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Hello from '@/components/Hello.vue'

export default {
  components: {
    Navbar,
    Hello
  }
  
}
</script>


<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #999;
  border: 2px solid #333;
  margin: 0;
  width: 100%;
}

</style>
