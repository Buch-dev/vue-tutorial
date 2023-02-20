<template>
  <div>
    <!-- Options API -->
    <input type="text" placeholder="First Name" v-model="fName" />
    <input v-model="lName" type="text" placeholder="Last Name" />

    <input v-model="heroName" type="text" placeholder="Hero Name" />
    <input v-model="firstName" type="text" placeholder="First Name" />
    <input v-model="lastName" type="text" placeholder="Last Name" />
  </div>
</template>

<script>
import { ref, reactive, toRefs } from "vue";
export default {
  name: "VModel",
  setup() {
    const heroName = ref("");
    const state = reactive({
      firstName: "",
      lastName: "",
    });

    return {
      heroName,
      ...toRefs(state),
    };
  },
  data() {
    return {
      fName: "",
      lName: "",
    };
  },
};
</script>

<style scoped></style>
