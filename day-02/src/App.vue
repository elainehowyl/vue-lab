<template>
  <div id="app">
     <DataForm></DataForm>
     <SignupForm></SignupForm>
     <FormValidation></FormValidation>
     <Services></Services>
  </div>
</template>

<script>

import DataForm from "./components/DataForm"
import SignupForm from "./components/SignupForm"
import FormValidation from "./components/FormValidation"
import Services from "./components/Services"

export default {
  name: 'App',
  components: {
     DataForm, SignupForm, FormValidation, Services
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
