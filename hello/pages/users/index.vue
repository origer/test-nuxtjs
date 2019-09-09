<template>
  <div>
    {{users}}
  </div>
</template>

<script>
  const axios = require('axios')
  let url = 'https://jsonplaceholder.typicode.com/users'

  export default {
    asyncData({params, error}) {
      return axios.get(url)
        .then((res) => {
            return {users: res.data}
        })
        .catch((e => {
          // console.log(e.response.status)
          error({ users: e.response.status,
                  message: e.message })
        }))
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
