<template>
  <div id="app">
    <form @submit="submitForm">
      <label for="name">Enter Name</label>
      <br />
      <input type="text" id="name" v-model="formValues.name" />
      <br />
      <label for="summery">Profile summery</label>
      <br />
      <textarea
        v-model="formValues.summery"
        name=""
        id="summery"
        cols="30"
        rows="10"
      ></textarea>

      <br />
      <label for="country"> Country </label>
      <select id="country" v-model="formValues.country">
        <option value="">SELECT Country</option>
        <option value="BD">Bangladesh</option>
        <option value="IN">India</option>
        <option value="NE">Nepal</option>
        <option value="MA">Maldivs</option>
        <option value="JA">Japan</option>
      </select>

      <hr />

      <label for="country"> Job Location </label>
      <select id="country" multiple v-model="formValues.jobLocation">
        <option value="">SELECT Country</option>
        <option value="BD">Bangladesh</option>
        <option value="IN">India</option>
        <option value="NE">Nepal</option>
        <option value="MA">Maldivs</option>
        <option value="JA">Japan</option>
      </select>

      <div>
        <input
          type="checkbox"
          id="remotework"
          v-model="formValues.remoteWork"
        />
        <label for="remotework">Remote Work?</label>

        <br />
        <input
          type="checkbox"
          id="located"
          v-model="formValues.located"
          true-value="yes"
          false-value="no"
        />
        <label for="located">Located In Dhaka</label>
      </div>

      <div>
        <p>Skill Set</p>
        <input
          type="checkbox"
          value="html"
          v-model="formValues.skillset"
          id="html"
        />
        <label for="html">HTML</label>
        <br />
        <input
          type="checkbox"
          value="css"
          v-model="formValues.skillset"
          id="css"
        />
        <label for="css">CSS</label>
        <br />
        <input
          type="checkbox"
          value="javascript"
          v-model="formValues.skillset"
          id="javascript"
        />
        <label for="javascript">Javascript</label>
        <br />

        <p>Years of Experience</p>
        <input
          type="radio"
          value="0-2"
          v-model="formValues.yearsOfEx"
          id="0-2"
        />
        <label for="0-2">0 -2</label>
        <br />

        <input
          type="radio"
          value="3-5"
          v-model="formValues.yearsOfEx"
          id="3-5"
        />
        <label for="3-5">3-5</label>
        <br />

        <input
          type="radio"
          value="5-7"
          v-model="formValues.yearsOfEx"
          id="5-7"
        />
        <label for="5-7">5-7</label>
        <br />

        <p>{{ formValues.yearsOfEx }}</p>

        <button type="submit">submit</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      formValues: {
        name: "",
        summery: "",
        country: "",
        jobLocation: [],
        remoteWork: false,
        located: "no",
        skillset: [],
        yearsOfEx: "",
      },
    };
  },
  methods: {
    submitForm(event) {
      event.preventDefault();
      console.log("Form Values", this.formValues);
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  color: red;
}
.bg-fine {
  background: #2c3e50;
}
</style>
