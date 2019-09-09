<template>
  <div class="container">
    <h1>{{ title }}</h1><br>
    <p>{{ message }}</p><br>
    <p>id: {{ this.$route.params.id }}</p><br>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'user page',
      message: 'user page'
    }
  },
  validate({ params }) {
    return /^\d+$/.test(params.id)
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
