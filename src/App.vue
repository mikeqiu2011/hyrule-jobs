<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('mike')">change name</button>
    <button @click="changeAge('19')">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  setup() {
    const state = reactive({
      name: "Link",
      age: 25 as number | string,
    });

    return { ...toRefs(state) };
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
