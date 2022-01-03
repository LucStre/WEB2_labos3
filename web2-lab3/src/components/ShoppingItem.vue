<template>
  <li class="shopping-item" :class="{ completed: completed }">
    <input
      class="toggle"
      type="checkbox"
      :checked="completed"
      @input="$emit('update:completed', $event.target.checked)"
    />

    <ShoppingList :title="title" />

    <button class="destroy" @click="$emit('destroy')">❌</button>
  </li>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ShoppingList from "@/components/ShoppingList.vue";

export default defineComponent({
  name: "ShoppingItem",
  props: {
    completed: Boolean,
    title: String,
  },
  components: {
    ShoppingList,
  },
  emits: ["update:completed"],
});
</script>

<style scoped>
.todo-item {
  padding: 8px;
  display: flex;
  align-items: center;
}

.todo-item label {
  flex: 1;
}

.todo-item.completed label {
  text-decoration: line-through;
}

.todo-item button {
  background: none;
  border: none;
  color: white;
  padding: 8px;
  font-weight: bold;
  cursor: pointer;
}
</style>
