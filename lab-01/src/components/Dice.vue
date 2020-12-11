<template>
<div>
    <div v-if="GeneratedNo%2 == 0">
        <div v-if="GeneratedNo == 6">
            <p v-bind:style="{'color':'green'}">{{GeneratedNo}}!</p>
        </div>
        <div v-else>
            <p>{{GeneratedNo}}!</p>
        </div>
    </div>
    <div v-else>
        <div v-if="GeneratedNo == 1">
           <p v-bind:style="{'color':'red'}">{{GeneratedNo}}</p>
        </div>
        <div v-else>
            <p>{{GeneratedNo}}</p>
        </div>
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