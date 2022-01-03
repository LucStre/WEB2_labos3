<template>
  <h1>{{ msg }}</h1>
</template>

<script>
import { onMounted, onBeforeUnmount } from "vue";

export default {
  name: "ShoppingList",
  props: {
    msg: String,
  },
  setup() {
    onMounted(async () => {
      alert("Welcome to shopping list!");
    });
    onBeforeUnmount(async () => {
      alert("You are leaving shoping list, bye-bye!");
    });
  },
};
</script>
