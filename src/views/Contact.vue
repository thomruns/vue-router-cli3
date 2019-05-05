<template>
  <div class="contact">
    <h1>This is a contact page</h1>
    <Hello msg="This is imported from Hello.vue"/>
  </div>
</template>

<script>
import Hello from '@/components/Hello.vue'

export default {
  name: 'contact',
  components: {
    Hello
  },
  props: {
    msg: String
  }
}
</script>

<style>
.contact {
  background: rgb(153, 109, 109);
  margin: 5px;
  border: 2px solid rgb(46, 34, 34);
}
</style>