<template>
  <div>
    <h3>Catgories</h3>
    <div class="categories">
      <div
        class="category"
        v-for="item in allCategories"
        :key="item.id"
        :class="{ selected: item.isSelected }"
        @click="item.isSelected = !item.isSelected"
      >
        <font-awesome-icon :icon="item.image" class="fa-2x" />
        <p>{{ item.name }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Categories",
  data() {
    return {
      allCategories: [
        {
          name: "City tours",
          image: "bus-alt",
          id: 1,
          isSelected: true,
        },
        {
          name: "Architechture",
          image: "store",
          id: 2,
          isSelected: false,
        },
        {
          name: "Cycling",
          image: "biking",
          id: 3,
          isSelected: false,
        },
        {
          name: "Driving",
          image: "truck-monster",
          id: 4,
          isSelected: false,
        },
        {
          name: "Educational",
          image: "book-open",
          id: 5,
          isSelected: false,
        },
        {
          name: "Haunted",
          image: "ghost",
          id: 6,
          isSelected: false,
        },
        {
          name: "Food",
          image: "utensils",
          id: 7,
          isSelected: false,
        },
        {
          name: "Heritage",
          image: "fan",
          id: 8,
          isSelected: true,
        },
        {
          name: "Nature",
          image: "tree",
          id: 9,
          isSelected: false,
        },
        {
          name: "Shopping",
          image: "shopping-bag",
          id: 10,
          isSelected: false,
        },
        {
          name: "Walking",
          image: "walking",
          id: 11,
          isSelected: true,
        },
        {
          name: "Accessible",
          image: "wheelchair",
          id: 12,
          isSelected: false,
        },
        {
          name: "For kids",
          image: "child",
          id: 13,
          isSelected: false,
        },
        {
          name: "Rivers",
          image: "water",
          id: 14,
          isSelected: false,
        },
        {
          name: "Hotels",
          image: "hotel",
          id: 15,
          isSelected: false,
        },
        {
          name: "Trains",
          image: "subway",
          id: 16,
          isSelected: false,
        },
        {
          name: "Described",
          image: "code-branch",
          id: 17,
          isSelected: false,
        },
        {
          name: "Easter Hunt",
          image: "egg",
          id: 18,
          isSelected: false,
        },
        {
          name: "Art & Culture",
          image: "paint-brush",
          id: 19,
          isSelected: false,
        },
        {
          name: "Entertainment",
          image: "music",
          id: 20,
          isSelected: false,
        },
        {
          name: "Life Journey",
          image: "dna",
          id: 21,
          isSelected: false,
        },
        {
          name: "Religious",
          image: "torii-gate",
          id: 22,
          isSelected: false,
        },
      ],
    };
  },
};
</script>
<style>
@import "./Categories.css";
</style>