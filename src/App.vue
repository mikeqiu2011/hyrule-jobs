<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('mike')">change name</button>
    <button @click="changeAge('19')">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  setup() {
    const name = ref("Link");
    const age = ref<number | string>(25);

    age.value = 30;

    return { name, age };
  },
  methods: {
    changeName(name: string) {
      this.name = name;
    },
  },
});
</script>

<style>
</style>
