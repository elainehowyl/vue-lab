<template>
<div>
    <div v-if="GeneratedNo%2 == 0">
        <p>{{GeneratedNo}}!</p>
    </div>
    <div v-else>
        <p>{{GeneratedNo}}</p>
    </div>
    <button @click="randomNo">Generate Number</button>
    <!-- <p>{{GeneratedNo}}</p> -->
</div>
</template>
<script>
export default{
    data:function(){
        return{
            GeneratedNo:0
        }
    },
    methods: {
        "randomNo":function(){
            this.GeneratedNo = Math.floor(Math.random() * 6) + 1;
        }
    }
}
</script>
<style></style>