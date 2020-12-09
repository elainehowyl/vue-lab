<template>
<div>
  <h1>{{greetings}}</h1>
  <button v-on:click="buttonPrint">Say Hi</button>
  <button v-on:click="buttonPrint2">Say goodbye</button>
  <button v-on:click="buttonSleep">Sleep</button>
</div>
</template>

<script>
export default{
    data: function(){
        return{
            // 'greetings':'Hello World'
        }
    },
    props:['greetings'],
    methods:{
        'buttonPrint':function(){
            this.greetings = "Hello World"
        },
        'buttonPrint2':function(){
            this.greetings = "Goodbye World"
        },
        'buttonSleep':function(){
            this.greetings = "zzz...zzz...zzz..."
        }
    }
}
</script>
<style></style>