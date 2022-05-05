<template>
  <div class="main">
    <IconUser></IconUser>
    <div class="row distance grid grid-rows-2">
      <div class="row border-gray-400 border-b border-dashed pt-2">
        <label for="input-from" class="text-gray-400 text-sm">From</label>
      </div>
      <div class="row pt-2">
        <label for="input-to" class="text-gray-400 text-sm">To</label>
      </div>
      <el-button class="distance-icon">
        <img
          src="@/assets/images/icon-two-arrow.svg"
          alt="icon-swap"
          width="100%"
          height="100%"
        />
      </el-button>
    </div>
    <div class="row flex justify-between">
      <el-button type="info" icon="el-icon-warning-outline"></el-button>
      <el-button type="primary" class="flex-1">Continue</el-button>
    </div>
    <BannerAds></BannerAds>
    <div class="row grid grid-cols-4 mt-10">
      <embed src="@/assets/images/icon-train.svg" class="mx-auto" />
      <embed src="@/assets/images/icon-bookmark.svg" class="mx-auto" />
      <embed src="@/assets/images/icon-ticket.svg" class="mx-auto" />
      <embed src="@/assets/images/icon-setting.svg" class="mx-auto" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import BannerAds from '~/components/order-ticket/bannerAds.vue';
import IconUser from '~/components/order-ticket/IconUser.vue';

interface Head {
  title: string;
  bodyAttrs: {
    class: string;
  };
}
export default Vue.extend({
  components: { IconUser, BannerAds },
  data() {
    return {};
  },
  head(): Head {
    return {
      title: 'Home | Training Booking App',
      bodyAttrs: {
        class: 'train-booking-app',
      },
    };
  },

  mounted() {},
});
</script>
