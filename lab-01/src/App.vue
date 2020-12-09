<template>
  <div id="app">
    <messageBox></messageBox>
    <h1>Goodbye World</h1>
  </div>
</template>

<script>

import messageBox from "./components/messageBox"

export default {
  name: 'App',
  components: {
     messageBox
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
