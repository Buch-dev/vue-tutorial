<template lang="">
  <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
  <h2>Computed fullname {{ fullName }}</h2>
  <button @click="changeFullName">Change Fullname</button>
  <button @click="items.push({ id: 4, title: 'Keyboard', price: 500 })">
    Add Item
  </button>
  <h2>Computed Total - {{ total }}</h2>
  <h2>Method Total - {{ getTotal() }}</h2>
  <input type="text" v-model="country" />

  <template v-for="item in items" :key="item.id"
    ><h2 v-if="item.price > 100">
      {{ item.title }} {{ item.price }}
    </h2></template
  >

  <h2 v-for="item in expensiveItems" :key="item.id">
    {{ item.title }} {{ item.price }}
  </h2>
</template>
<script>
export default {
  data() {
    return {
      firstName: "Bruce",
      lastName: "Wayne",
      items: [
        {
          id: 1,
          title: "TV",
          price: 100,
        },
        {
          id: 2,
          title: "Phone",
          price: 200,
        },
        {
          id: 3,
          title: "Laptop",
          price: 300,
        },
      ],
      country: "",
    };
  },
  methods: {
    getTotal() {
      console.log("getTotal Method");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
    changeFullName() {
      this.fullName = 'Clark Kent'
    }
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`;
      },
      set(value) {
        const names = value.split(' ')
        this.firstName = names[0]
        this.lastName = names[1]
      }
    },
    total() {
      console.log("total computed property");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
    expensiveItems() {
      return this.items.filter(item => item.price > 100);
    },
  },
};
</script>
<style lang=""></style>
