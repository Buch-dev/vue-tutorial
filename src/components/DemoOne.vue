<template>
  <div>
    <h2>{{ name }}</h2>
  </div>
</template>

<script>
import {ref} from 'vue'
export default {
  name: "DemoOne",
  setup() {
    const name = ref("Buchman");

    setTimeout(() => {
      name.value = "Buchcodx";
      console.log(name.value);
    }, 2000);

    return {
      name,
    };
  },
};
</script>

<style scoped></style>
