<template>
  <div>
      <label>Services Customisation: </label>
      <input type="checkbox" value="birthday song" v-model="services"><label>Birthday Song ($3.00)</label>
      <input type="checkbox" value="birthday cake" v-model="services"><label>Birthday Cake ($20.00)</label>
      <input type="checkbox" value="animal mascot" v-model="services"><label>Animal Mascot ($30.00)</label>
      <input type="checkbox" value="door gift" v-model="services"><label>Special Door-gift ($5.00)</label>
      <h2>Total Cost: {{displayTotalCost}}</h2>
  </div>
</template>
<script>
export default{
    data:function(){
        return{
            services:[],
        }
    },
    computed:{
        'displayTotalCost':function(){
            let totalCost = 0;
            let servicesList = {
                "birthday song":3.00,
                "birthday cake":20.00,
                "animal mascot":30.00,
                "door gift":5.00
            }
            for(let eachSer of this.services){
                for(let eachSerInList in servicesList){
                    if(eachSer == eachSerInList){
                        totalCost += servicesList[eachSerInList]
                    }
                }
            }
            return totalCost;
        }
    }
}
</script>
<style></style>