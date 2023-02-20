<template lang="">
  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'Bruce'">{{ name }}</h2>
    <h2 v-if="name === 'Clark'">{{ name }}</h2>
  </template>
</template>
<script>
export default {
  data() {
    return {
      names: ["Bruce", "Clark", "Diana"],
    };
  },
};
</script>
<style lang=""></style>
