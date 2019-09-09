<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <p>{{ message }}</p>
    <p>
      <router-link to="/">Index Page</router-link>
    </p>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'Price Page',
      message: 'Hello World!'
    }
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
