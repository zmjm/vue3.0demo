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
    console.log(process.env.VUE_APP_APIURL);
  },
  setup() {
    const count = ref("'s'");
    const add = () => {
      count.value = count.value + "'b'";
    };
    return {
      count,
      add
    };
  }
};
</script>
