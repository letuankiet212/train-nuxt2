<template>
  <div>
    <div v-for="(movie, index) in moves_list" :key="'movie' + index">
      {{ movie }}
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

const FEATURE_API =
  'https://api.themoviedb.org/3/movie/550?api_key=bca49a093b3e8e9ad79c022892716ab8';

export default Vue.extend({
  name: 'HomeMovie',

  async asyncData({ $axios }: any) {
    console.log($axios);
    const data = await $axios.$get(FEATURE_API);
    try{

    }then
    console.log(data);

    return data;
  },
  data() {
    return {
      moves_list: [1, 2, 3] as Array<Number>,
    };
  },
  computed: {
    hello(): string {
      return 'hello';
    },
  },
});
</script>
