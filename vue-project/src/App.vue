<template>
    <div id="app">
      <input type="text" v-model="searchText"
      placeholder="Search..">
      <list :items="items" :searchText="searchText"></list>
    </div>
</template>

<script>
import list from './components/list.vue';
export default {
  name: "App",
  components: { list },
  data() {
    return {
      searchText: '',
      items: [
      {
    "id": "1",
    "name": "Smartphone X1",
    "description": "High-quality smartphone with dual-camera",
    "availability": "In Stock",
    "price": 599.99
  },
  {
    "id": "2",
    "name": "Electric Toothbrush",
    "description": "Advanced bristle technology for a better clean",
    "availability": "Out of Stock",
    "price": 49.99
  },
      ]
    }
  },
};
</script>




