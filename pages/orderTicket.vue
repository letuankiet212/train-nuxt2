<template>
  <div class="main">
    <div class="row flex">
      <p class="flex-1 font-Gilroy-Bold text-3xl">Where do you want to go ?</p>
      <el-avatar
        :size="66"
        :src="require(`~/assets/images/Avatar.png`)"
        @error="errorHandler"
        class="p-3"
      >
        <img
          src="https://cube.elemecdn.com/e/fd/0fc7d20532fdaf769a25683617711png.png"
        />
      </el-avatar>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

interface Head {
  title: string
  bodyAttrs: {
    class: string
  }
}

export default Vue.extend({
  head(): Head {
    return {
      title: 'Home | Training Booking App',
      bodyAttrs: {
        class: 'train-booking-app',
      },
    }
  },
  methods: {
    errorHandler() {
      return true
    },
  },
})
</script>
