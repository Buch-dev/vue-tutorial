<template>
  <div>
    <!-- Options API -->
    <input v-model="name" type="text" placeholder="Name" />

    <input v-model="firstName" type="text" placeholder="First Name" />
    <input v-model="lastName" type="text" placeholder="Last Name" />

    <input v-model="fName" type="text" placeholder="Reactive First Name" />
    <input v-model="lName" type="text" placeholder="Reactive Last Name" />
    <input
      v-model="options.heroName"
      type="text"
      placeholder="Reactive Hero Name"
    />
  </div>
</template>

<script>
import { ref, watch, reactive, toRefs } from "vue";
import _ from "lodash";

export default {
  name: "WatchCompositionAPI",
  setup() {
    const state = reactive({
      fName: "",
      lName: "",
      options: {
        heroName: "",
      },
    });

    // watch(
    //   () => {
    //     return { ...state };
    //   },
    //   function (newValue, oldValue) {
    //     console.log("fName Old value", oldValue.fName);
    //     console.log("fName New value", newValue.fName);
    //     console.log("lName Old value", oldValue.lName);
    //     console.log("lName New value", newValue.lName);
    //   }
    // );

    watch(
      () => _.cloneDeep(state.options),
      function (newValue, oldValue) {
        console.log("fName Old value", oldValue);
        console.log("fName New value", newValue);
      },
      {
        deep: true,
      }
    );

    const firstName = ref("");
    const lastName = ref("Wayne");

    watch(
      [firstName, lastName],
      (newValues, oldValues) => {
        console.log("firstName Old value", oldValues[0]);
        console.log("firstName New value", newValues[0]);
        console.log("lastName Old value", oldValues[1]);
        console.log("lastName New value", newValues[1]);
      },
      {
        immediate: true,
      }
    );

    return {
      firstName,
      lastName,
      ...toRefs(state),
    };
  },
  data() {
    return {
      name: "",
    };
  },
  watch: {
    name(newValue, oldValue) {
      console.log("Old value", oldValue);
      console.log("New value", newValue);
    },
  },
};
</script>

<style scoped></style>
