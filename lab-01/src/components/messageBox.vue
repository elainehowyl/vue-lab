<template>
<!-- inside template, you can only have one parent element -->
 <div>
     <h1 v-bind:style="{'backgroundColor':bgcolor}">{{message}}</h1>
 </div>
</template>
<script>
export default {
    data: function(){
        return {
            // 'message':' '
        }
    },
    props:['message', 'bgcolor']
}
</script>
<style scoped>
div{
    background-color:pink;
}
</style>