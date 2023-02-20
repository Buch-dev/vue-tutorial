<template lang="">
  <h2 v-once>{{ name }}</h2>
  <button @click="name = 'Batman'">Change name</button>
  <h2 v-pre>{{name}}</h2>
</template>
<script>
export default {
  data() {
    return {
      name: "Buchman",
    };
  },
};
</script>
<style lang=""></style>
