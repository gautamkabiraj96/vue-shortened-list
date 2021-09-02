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
  name: "ShortenedList",
  data() {
    return {
      myList: [
        "Koenigsegg Jesko Absolut",
        "Bugatti Chiron Super Sport",
        "SSC Tuatara",
        "Hennessey Venom F5",
        "Aston Martin Valkyrie",
        "McLaren Speedtail",
        "Koenigsegg Gemera",
        "Pagani Huayra BC Roadster",
        "Rimac Concept_One",
        "Lamborghini Sian Roadster",
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