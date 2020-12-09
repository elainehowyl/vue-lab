<template>
<!-- inside template, you can only have one parent element -->
 <div>
     <div>Welcome</div>
     <div>{{message}}</div>
 </div>
</template>
<script>
export default {
    data: function(){
        return {
            'message':'very hello world'
        }
    }
}
</script>
<style scoped>
div{
    background-color:pink;
}
</style>