<template>
  <div>
    <div v-if="oddOrEven%2 == 0">
        Number is even!
        <h1 v-bind:style="{'color':'green'}">{{oddOrEven}}</h1>
    </div>
    <div v-else>
        Number is odd!
        <h1 v-bind:style="{'color':'red'}">{{oddOrEven}}</h1>
    </div>
    <!-- <h1 v-bind:style="{'backgroundColor':bgcolor}">{{oddOrEven}}</h1> -->
    <button v-on:click="Increment">+</button>
    <button v-on:click="Decrement">-</button>
  </div>
</template>
<script>
export default{
    data:function(){
        return{
            oddOrEven:0
        }
    },
    // props:['oddOrEven'],
    methods:{
        'Increment':function(){
            this.oddOrEven += 1
        },
        'Decrement':function(){
            this.oddOrEven -= 1
        }
    }
}
</script>
<style>
</style>