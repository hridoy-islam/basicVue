<template>
  <div id="app">
    <p v-if="count === 0">Its Zero</p>
    <p v-else-if="count < 2">its grater Than 0</p>
    <p v-else-if="count > 5">its less Than 5</p>
    <p v-else>Its Else</p>
    <div v-if="display">
      <button>Go Back</button>
      <button>Visit Now</button>
    </div>
    <h1 v-show="show">Show V-SHow elemeent</h1>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      count: "nothing",
      display: false,
      show: true,
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
