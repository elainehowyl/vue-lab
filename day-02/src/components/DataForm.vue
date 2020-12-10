
<template>
  <div>
    <form>
      <div>
        <label>First Name </label>
        <input type="text" v-model="first_name" />
        <label>Last Name </label>
        <input type="text" v-model="last_name" />
      </div>
      <div>
          <label>Gender </label>
          <input type="radio" value="male" v-model="gender"/>Male
          <input type="radio" value="female" v-model="gender"/>Female
      </div>
      <div>
          <label>Occupation </label>
          <input type="radio" value="students" v-model="occupation"/>Students
          <input type="radio" value="part-time" v-model="occupation"/>Part Time
          <input type="radio" value="full-time" v-model="occupation"/>Full Time
      </div>
      <div>
          <label>Interests</label>
          <input type="checkbox" value="reading" v-model="interests"><label>Reading</label>
          <input type="checkbox" value="sleeping" v-model="interests"><label>Sleeping</label>
          <input type="checkbox" value="music" v-model="interests"><label>Music</label>
          <input type="checkbox" value="tv" v-model="interests"><label>Watch TV</label>
     </div>
     <div>
          <label>Leisure</label>
          <input type="checkbox" value="reading" v-model="leisure"><label>Reading</label>
          <input type="checkbox" value="sleeping" v-model="leisure"><label>Sleeping</label>
          <input type="checkbox" value="sports" v-model="leisure"><label>Sports</label>
          <input type="checkbox" value="eating" v-model="leisure"><label>Eating</label>
          <input type="checkbox" value="Hanging out with friends" v-model="leisure"><label>Hanging out with friends</label>
     </div>
     <div>
        <label>How did you hear about us? </label>
        <select v-model="hearabout">
            <option value="friends">From friends</option>
            <option value="facebook">From Facebook</option>
            <option value="email">From Email</option>
        </select>
    </div>
    <div>
        <label>Which country are you from? </label>
        <select v-model="country">
            <option value="Singapore">Singapore</option>
            <option value="Malaysia">Malaysia</option>
            <option value="Thailand">Thailand</option>
            <option value="Indonesia">Indonesia</option>
        </select>
    </div>
    <!-- v-model.number is to change data type from string to number -->
    <div>
        <label>First Number: </label>
        <input type="number" v-model.number="first_num"/>
        <label>Second Number: </label>
        <input type="number" v-model.number="second_num"/>
    </div>
    </form>
    <div>
      <h1>Your details</h1>
      <ul>
        <li>First Name: {{ first_name }}</li>
        <li>Last Name: {{ last_name }}</li>
        <li>Gender: {{gender}} </li>
        <li>Occupation: {{occupation}} </li>
        <li>Interests: {{interests}} </li>
        <li>Leisure: {{leisure}} </li>
        <li>Where did you hear about us? {{hearabout}} </li>
        <li>Country of Origin: {{country}} </li>
      </ul>
      <button v-on:click="addition">Add</button>
      <p> Addition: {{displayAddition}} </p>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      first_name: "",
      last_name: "",
      gender: "",
      occupation: "",
      interests: [],
      leisure: [],
      hearabout: "",
      country: "",
      first_num: 0,
      second_num: 0,
      displayAddition: 0,
    };
  },
  methods:{
      'addition': function(){
          this.displayAddition = this.first_num + this.second_num
      }
  }
};
</script>
<style></style>