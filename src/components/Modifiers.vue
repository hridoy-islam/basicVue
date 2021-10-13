<template>
  <div id="app">
    <form @submit.prevent="submitform">
      <label for="">Name</label>
      <input type="text" v-model.trim.lazy="formValues.name" />
      <p>{{ formValues.name }}</p>

      <label>age</label>
      <input
        @keyup.enter="submitform"
        type="text"
        v-model.number="formValues.age"
      />
      <p>{{ formValues.age }}</p>
      <br />
      <br />
      <!--  <button type="submit">Submit</button> -->
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
        age: null,
      },
    };
  },
  methods: {
    submitform() {
      // event.preventDefault();
      console.log("Form Data", this.formValues);
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
