<template>
  <div class="flex">
    <p class="flex-1 font-Gilroy-Bold text-3xl">Where do you want to go ?</p>
    <el-avatar
      :size="66"
      :src="require(`~/assets/images/Avatar.png`)"
      class="p-3"
      @error="errorHandler"
    >
      <img
        src="https://cube.elemecdn.com/e/fd/0fc7d20532fdaf769a25683617711png.png"
      />
    </el-avatar>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'IconUser',
  methods: {
    errorHandler() {
      return true;
    },
  },
});
</script>
