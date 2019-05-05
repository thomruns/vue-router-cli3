<template>
  <div class="hello">
    <h3>{{ msg }}</h3>
  </div>
</template>

<script>
export default {
  name: 'Hello',
  props: {
    msg: String
  }
}
</script>

<style>
.hello {
  background: #ccc;
  border: 2px solid #888;
  margin: 5px;
}
</style>
