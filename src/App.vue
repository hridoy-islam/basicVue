<template>
  <div id="app">
    <template v-for="name in names">
      <h3>{{ name }}</h3>
      <input type="text" name="" placeholder="Last name" />
      <hr />
    </template>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["Ridoy", "Guy", "Mohammad", "Tisha"],
    };
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
