<template>
  <div>
    <div v-for="(movie, index) in moves_list" :key="'movie' + index">
      {{ movie }}
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'HomeMovie',
  data() {
    return {
      moves_list: [1, 2, 3] as Array<Number>,
    };
  },
});
</script>
