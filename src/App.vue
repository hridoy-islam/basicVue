<template>
  <div id="app">
    <h1>{{ 2 + 3 + 5 }}</h1>
    <h1>{{ 5 + 3 + 15 }}</h1>
    <h2>{{ add(2, 3, 5) }}</h2>
    <h2>{{ add(12, 23, 15) }}</h2>
    <h2>{{ multiply(baseNum) }}</h2>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["Ridoy", "Guy", "Mohammad", "Tisha"],
      baseValue: 10,
      baseNum: 5,
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(value) {
      return value * this.baseValue;
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
