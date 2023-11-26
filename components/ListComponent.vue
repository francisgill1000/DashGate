<template>
  <v-list>
    <div class="px-5">
      <h2>List</h2>
    </div>
    <v-list-item v-for="(item, index) in items" :key="index">
      <v-list-item-content>
        <v-list-item-title>{{ item.name }}</v-list-item-title>
        <v-list-item-subtitle>{{ item.description }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
  </v-list>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        { text: "Name", value: "name" },
        { text: "Description", value: "description" },
      ],
      items: [
        { name: "Item 1", description: "Description for Item 1" },
        { name: "Item 2", description: "Description for Item 2" },
        { name: "Item 3", description: "Description for Item 3" },
        // Add more items as needed
      ],
    };
  },
};
</script>
