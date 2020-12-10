<template>
  <div id="app">
     <DataForm></DataForm>
     <SignupForm></SignupForm>
  </div>
</template>

<script>

import DataForm from "./components/DataForm"
import SignupForm from "./components/SignupForm"

export default {
  name: 'App',
  components: {
     DataForm, SignupForm
  }
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
