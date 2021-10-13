<template>
  <div id="app">
    <h4>Fullname - {{ fullName }}</h4>
    <h4>
      Total -
      {{ items.reduce((total, current) => (total = total + current.price), 0) }}
    </h4>

    <button @click="items.push({ id: 5, title: 'Bangi', price: 10 })">
      Add Item
    </button>

    <h4>Computed Price - {{ total }}</h4>
    <hr />

    <div v-for="item in items" :key="item.id">
      <h4 v-if="item.price > 10">{{ item.title }} - {{ item.price }}</h4>
    </div>

    <div v-for="item in expensiveItem" :key="item.id">
      <h1>{{ item.title }} {{ item.price }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstName: "Ridoy",
      lastName: "Islam",
      items: [
        { id: 1, title: "orange", price: 20 },
        { id: 2, title: "mango", price: 10 },
        { id: 3, title: "bannana", price: 40 },
        { id: 4, title: "apple", price: 10 },
      ],
    };
  },
  computed: {
    fullName() {
      return `${this.firstName}  ${this.lastName}`;
    },
    total() {
      return this.items.reduce(
        (total, current) => (total = total + current.price),
        0
      );
    },
    expensiveItem() {
      return this.items.filter((item) => item.price > 10);
    },
  },
};
</script>

<style>
</style>
