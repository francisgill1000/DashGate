<template>
    <v-data-table :headers="headers" :items="items" class="elevation-1"></v-data-table>

</template>

<script>
export default {
  data() {
    return {
      headers: [
        { text: 'Name', value: 'name' },
        { text: 'Description', value: 'description' },
      ],
      items: [
        { name: 'Item 1', description: 'Description for Item 1' },
        { name: 'Item 2', description: 'Description for Item 2' },
        { name: 'Item 3', description: 'Description for Item 3' },
        // Add more items as needed
      ],
    };
  },
};
</script>
