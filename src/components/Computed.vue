<template>
  <div>
    <!-- Options API -->
    <input v-model="fName" type="text" placeholder="First Name" />
    <input v-model="lName" type="text" placeholder="Last Name" />
    <h2>Options Fullname is {{ fullName }}</h2>

    <input v-model="refFirstName" type="text" placeholder="First Name" />
    <input v-model="refLastName" type="text" placeholder="Last Name" />
    <h2>Composition Fullname is {{ refFullName }}</h2>

    <input v-model="reactiveFirstName" type="text" placeholder="First Name" />
    <input v-model="reactiveLastName" type="text" placeholder="Last Name" />
    <h2>Reactive Fullname is {{ reactiveFullName }}</h2>
  </div>
</template>

<script>
import { ref, computed, reactive, toRefs } from "vue";
export default {
  name: "ComputedCompositionAPI",
  setup() {
    const refFirstName = ref("");
    const refLastName = ref("");

    const refFullName = computed(function() {
      return `${refFirstName.value} ${refLastName.value}`;
    });

    const state = reactive({
      reactiveFirstName: "",
      reactiveLastName: "",
    });

    const reactiveFullName = computed(function() {
      return `${state.reactiveFirstName} ${state.reactiveLastName}`;
    });

    return {
      refFirstName,
      refLastName,
      refFullName,
      ...toRefs(state),
      reactiveFullName
    };
  },
  data() {
    return {
      fName: "",
      lName: "",
    };
  },
  computed: {
    fullName() {
      return `${this.fName} ${this.lName}`;
    },
  },
};
</script>

<style scoped></style>
