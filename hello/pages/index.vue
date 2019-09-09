<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <p>{{ message }}</p>
    <p>
      <router-link to="/price">Price Page</router-link>
    </p>

  </div>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'Index page',
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

h1{
  display: block;
  border-bottom: 1px solid #ccc;
  margin: 2em ;
}

a{

  border: 1px solid #ccc;
  padding: 0.5em 0.7em;
}

p{
  display: block;
}
</style>
