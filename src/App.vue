<template>
  <div>
    <ul>
      <li v-for="(item, index) in getShortList(5)" :key="index">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Test",
  data() {
    return {
      myList: [
        "Item 1",
        "Item 2",
        "Item 3",
        "Item 4",
        "Item 5",
        "Item 6",
        "Item 7",
        "Item 8",
        "Item 9",
      ],
    };
  },
  methods: {
    getShortList(shortListSize) {
      return this.myList.slice(0, shortListSize);
    },
  },
};
</script>