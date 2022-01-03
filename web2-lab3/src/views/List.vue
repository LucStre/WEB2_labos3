<template>
  <div class="list">
    <ShoppingList msg="Welcome to shopping list" />
    <div v-if="loading">Loading...</div>
    <ul v-else class="shopping-list">
      <h2 v-if="boughtAll">You bought everything from your shopping list!</h2>

      <li class="new-shopping-item">
        <input @keyup.enter="addItem" id="new-shopping" v-model="newItem" />
        <button class="new-shopping-btn" @click="addItem">Add</button>
      </li>

      <ShoppingItem
        v-for="item in items"
        :key="item.id"
        :title="item.title"
        v-model:completed="item.completed"
      />
    </ul>
  </div>
</template>

<script>
// @ is an alias to /src
import ShoppingList from "@/components/ShoppingList.vue";
//import ShoppingItem from "@/components/ShoppingItem.vue";

/* interface IItem {
  id: number;
  title: string;
  completed: boolean;
}

let itemId = 1;

let _items: Array<IItem> = [
  {
    id: itemId++,
    completed: false,
    title: "Mlijeko",
  },
  {
    id: itemId++,
    completed: true,
    title: "Kruh",
  },
];*/

export default {
  name: "List",
  components: {
    ShoppingList,
  },
  /*data() {
    return {
      items: null as Array<ITodo> | null,
      loading: true,
      newItem: "",
    };
  },
  created() {
    this.fetchData();
  },
  computed: {
    boughtAll(): boolean {
      return !!this.items?.every((item) => item.completed);
    },
  },
  methods: {
    async fetchData() {
      this.items = await new Promise<Array<IItem>>((resolve) => {
        setTimeout(() => {
          resolve(_items);
        }, 1000);
      });
      this.loading = false;
    },
    addItem() {
      var value = this.newItem && this.newItem.trim();

      if (!value) {
        return;
      }

      this.items?.unshift({
        id: itemId++,
        title: value,
        completed: false,
      });
      this.newItem = "";
    },
    removeItem(item: IItem) {
      this.items = this.items?.filter((_item) => item !== _item) || null;
    },
  },*/
};
</script>
