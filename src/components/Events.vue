<template>
  <div id="app">
    <h2>{{ name }}</h2>
    <button @click="changeName">change name</button>

    <h2>Count {{ count }}</h2>
    <button @click="increment(1)">Increment</button>
    <button @click="increment(5)">Increment 5</button>
    <button @click="decrement(1)">Decrement</button>
    <button @click="decrement(5)">Decrement 5</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Ridoy",
      count: 0,
    };
  },
  methods: {
    increment(num) {
      return (this.count += num);
    },
    decrement(num) {
      return (this.count -= num);
    },
    changeName(event) {
      this.name = "Batman";
      console.log('Event', event);
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
