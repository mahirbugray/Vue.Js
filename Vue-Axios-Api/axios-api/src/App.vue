<template>
  <div>
    <Form />
  </div>
</template>

<script>

import Form from './components/Form.vue'

export default {
  name: 'App',
  components: {
    Form
  },
  data() {
    return {
      url: "https://65dc7515e7edadead7ec1361.mockapi.io/Deneme",
      list: []
    }
  },
  created() {
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
