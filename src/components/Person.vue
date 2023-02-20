<template>
  <div>
    <input v-model="firstName" type="text" placeholder="First Name" />
    <input v-model="lastName" type="text" placeholder="Last Name" />
  </div>
  <PersonGreeting :firstName="firstName" :lastName="lastName" @callHeroes="callHeroes" />
</template>

<script>
import { ref } from "vue";
import PersonGreeting from "./PersonGreeting.vue";
export default {
  name: "PersonC",
  components: {
    PersonGreeting,
  },
  setup() {
    const firstName = ref("");
    const lastName = ref("");

    function callHeroes(hero) {
        alert(`Calling ${hero}`)
    }

    return {
      firstName,
      lastName,
      callHeroes,
    };
  },
};
</script>

<style scoped></style>
