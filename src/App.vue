<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('mike')">change name</button>
    <button @click="changeAge('19')">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  data() {
    return {
      name: "Link",
      age: 25 as number | string, // type assertion, explicitly indicate types for Vue
    };
  },
  methods: {
    changeName(name: string) {
      this.name = name;
    },
    changeAge(age: number | string) {
      this.age = age;
    },
  },
});
</script>

<style>
</style>
