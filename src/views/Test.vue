<template>
  <div class="test">
    <h1>test count: {{ count }}</h1>
    <button @click="add">add</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  mounted() {
    this.add();
  },
  setup() {
    const count = ref("'s'");
    const add = () => {
      count.value = count.value + "'b'";
    };
    const a = 1;
    return {
      count,
      add,
      a
    };
  }
};
</script>
