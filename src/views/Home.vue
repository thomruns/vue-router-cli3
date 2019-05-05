<template>
  <div class="home">
    <h2>Home.vue</h2>
    <Hello msg="Hello.vue Component within Home.vue view"/>0
  </div>
</template>

<script>
// @ is an alias to /src
import Hello from '@/components/Hello.vue'

export default {
  name: 'home',
  components: {
    Hello
  }
}
</script>

<style>
.home {
  background: #aa55aa;
  height: 250px;
  border: 2px solid #000;
  margin: 5px;
}
</style>

