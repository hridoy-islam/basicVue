<template>
  <div id="app">
    <h1 v-once>{{ name }}</h1>
    <button @click="name = 'Batman'">Change Name</button>

    <h1 v-pre>{{ name }}</h1>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Ridoy Islam",
    };
  },
};
</script>

<style>
</style>
