<template>
  <div>
      <form>
          <label>Username: </label>
          <input type="text" v-model="username"/>
          <h2>{{usernameOk}}</h2>
          <label>Password: </label>
          <input type="text" v-model="password"/>
          <h2>{{passwordOk}}</h2>
      </form>
  </div>
</template>
<script>
export default{
    data: function(){
        return{
            username:"",
            password:"",
        }
    },
    computed:{
        'usernameOk':function(){
            if (this.username.length >= 7){
                return true;
            }
            else{
                return false;
            }
        },
        'passwordOk':function(){
            let specialChar='~!@#$%^&^*().'
            for(let each of specialChar){
                if(this.password.includes(each)){
                    return true;
                }
            }
            return false;
        }
    }
}
</script>
<style></style>