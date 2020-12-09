<template>
  <div id="app">
    <messageBox message="danger danger" bgcolor="green"></messageBox>
    <messageBox message="be careful" v-bind:bgcolor="preferredColor"></messageBox>
    <h1>{{text}}</h1>
    <button v-on:click="buttonPressed">Click</button>
    <input type="text" v-model='preferredColor'/>
    <Light></Light>
    <SayGreetings></SayGreetings>
    <Counter></Counter>
    <Dice></Dice>
  </div>
</template>

<script>

import messageBox from "./components/messageBox"
import Light from "./components/Light"
import SayGreetings from "./components/SayGreetings"
import Counter from "./components/Counter"
import Dice from "./components/Dice"

export default {
  name: 'App',
  components: {
     messageBox, Light, SayGreetings, Counter, Dice
  },
  data: function(){
      return {
          'text':'',
          'preferredColor':'azure'
      }
  },
  methods: {
      'buttonPressed':function(){
          this.text="You clicked me!"
      }
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
