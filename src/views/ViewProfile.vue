<template>
  <div class="view-profile">
    <h2>Profile for User: {{ userId }}</h2>
  </div>
</template>

<script>
export default {
  name: 'ViewProfile',
  data() {
    return {
      userId: this.$route.params.user_id
    }
  },
  methods: {
    updateId() {
      this.userId = this.$route.params.user_id
    }
  },
  watch: {
      $route: 'updateId'
    }
}
</script>

<style>
.view-profile {
  background-color: #668822;
  padding: 10px;
  border: 1px solid #fff;
  margin: 15px;
}

</style>
