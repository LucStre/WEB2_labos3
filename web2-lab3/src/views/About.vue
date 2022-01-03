<template>
  <div class="about">
    <h1>About page</h1>
  </div>
</template>

<script>
import { onMounted, onBeforeUnmount } from "vue";

export default {
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
