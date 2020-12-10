<template>
  <div>
    <form>
      <div>
        <label> Username: </label>
        <input type="text" v-model="username" />
      </div>
      <div>
          <label> Programming Background: </label>
          <input type="radio" v-model="programmingbg" value="No Experience"/>No Experience
          <input type="radio" v-model="programmingbg" value="Intermediate"/>Intermediate
          <input type="radio" v-model="programmingbg" value="Experienced"/>Experienced
      </div>
      <div>
          <label> Interested Programming Language: </label>
          <input type="checkbox" v-model="interestedprogram" value="Java"/>Java
          <input type="checkbox" v-model="interestedprogram" value="Python"/>Python
          <input type="checkbox" v-model="interestedprogram" value="C++"/>C++
          <input type="checkbox" v-model="interestedprogram" value="Javascript"/>Javascript
      </div>
      <div>
        <label>Preferred Timing </label>
        <select v-model="preferredtiming">
            <option value="morning">Morning</option>
            <option value="afternoon">Afternoon</option>
            <option value="evening">Evening</option>
        </select>
    </div>
    </form>
    <div>
      <p>Username: {{ username }}</p>
      <p>Programming Background: {{programmingbg}}</p>
      <p>Interested Programming Language: {{interestedprogram}}</p>
      <p>Preferred Timing: {{preferredtiming}}</p>
    </div>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      username: "",
      programmingbg: "",
      interestedprogram: [],
      preferredtiming: ""
    };
  },
};
</script>
<style></style>