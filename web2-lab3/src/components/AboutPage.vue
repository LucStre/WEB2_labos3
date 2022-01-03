<template>
  <h1>{{ msg }}</h1>
</template>

<script>
import { onMounted, onBeforeUnmount } from "vue";

export default {
  name: "AboutPage",
  props: {
    msg: String,
  },
  setup() {
    onMounted(async () => {
      alert("Welcome to about page!");
    });
    onBeforeUnmount(async () => {
      alert("You are leaving about page, bye-bye!");
    });
  },
};
</script>
