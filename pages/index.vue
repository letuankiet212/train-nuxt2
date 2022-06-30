<template>
  <div class="bg-phone">
    <div id="home_page">
      <div class="home__head px-2">
        <div class="home__head--line1 flex items-center">
          <div class="home__head-avatar flex-1">
            <img src="~/assets/images/Avatar.png" />
          </div>

          <div class="home__head--btn-cread text-center">
            <el-button
              icon="el-icon-search"
              class="w-9 h-9 p-0 font-bold"
              @click="search.status = !search.status"
            ></el-button>
          </div>

          <div class="home__head--btn-reload text-center ml-2">
            <el-button
              icon="el-icon-s-tools"
              class="w-9 h-9 p-0 font-bold"
            ></el-button>
          </div>
        </div>
        <el-collapse-transition>
          <div v-show="search.status" class="home__head--line2 mb-2">
            <el-input v-model="search.params" placeholder="Type something">
              <i slot="prefix" class="el-input__icon el-icon-search"></i>
            </el-input>
          </div>
        </el-collapse-transition>
      </div>
      <hr />
      <div class="home__content">
        <div
          class="shop-info bg-white m-2 rounded-lg shadow-lg border-solid border-gray-100 border"
        >
          <div
            class="shop__name border-b border-gray-300 border-solid mb-1 bg-orange-primary text-white p-1 rounded-t-lg"
          >
            <i class="el-icon-s-shop"></i>
            <span>Cửa Hàng: KietStore - Thành Phố Đà Nẵng</span>
          </div>
          <div class="px-1 pb-1">
            <div class="shop__banner">
              <div class="block">
                <el-carousel trigger="click" height="150px">
                  <el-carousel-item
                    v-for="item in 4"
                    :key="item"
                    class="bg-gray-200"
                  >
                    <img src="~/assets/images/banner-food.png" alt="" />
                  </el-carousel-item>
                </el-carousel>
              </div>
            </div>
            <!-- <div class="shop__descript mt-2">
            <span
              style="font-size: 10px"
              class="text-white bg-red-500 p-1 rounded-lg font-bold leading-none"
              >Yêu thích +</span
            >
            <span class="leading-normal"
              >Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis
              eos ex repellendus autem sapiente sint ut facilis consequatur a
              debitis?</span
            >
          </div> -->
            <div class="shop__stat mt-2">
              <div
                class="shop__stat--line1 flex justify-between items-end pb-2 mb-2 border-b border-gray-400 border-solid"
              >
                <div class="shop__stat--reaction flex items-center">
                  <div class="icon--reaction text-center">
                    <div class="icon h-6 w-6 mx-auto">
                      <img
                        src="~/assets/images/good_active.png"
                        class="w-full h-full"
                        alt=""
                      />
                    </div>
                  </div>
                  <div class="icon--reaction text-center">
                    <div class="icon h-6 w-6 mx-auto">
                      <img
                        src="~/assets/images/natural_active.png"
                        class="w-full h-full"
                        alt=""
                      />
                    </div>
                  </div>
                  <div class="icon--reaction text-center">
                    <div class="icon h-6 w-6 mx-auto">
                      <img
                        src="~/assets/images/disappointed_active.png"
                        class="w-full h-full"
                        alt=""
                      />
                    </div>
                  </div>
                  <div class="icon--reaction text-center">
                    <div class="icon h-6 w-6 mx-auto">
                      <img
                        src="~/assets/images/hate_active.png"
                        class="w-full h-full"
                        alt=""
                      />
                    </div>
                  </div>
                  <div class="ml-2 pt-1 text-gray-400">22</div>
                </div>
                <div
                  class="shop__stat--total-comment text-gray-400 cursor-pointer"
                >
                  4,5k bình luận
                </div>
              </div>
              <div class="shop__stat--line2 flex justify-between items-center">
                <div class="icon-like relative">
                  <el-button icon="el-icon-thumb" size="mini">Like</el-button>
                  <div
                    class="list-icon absolute bg-white rounded-xl shadow-lg px-3 py-1 w-auto border border-gray-200 border-solid gap-1"
                  >
                    <img
                      class="block hover:scale-125 ease-in duration-300 cursor-pointer"
                      src="~/assets/images/excellent.gif"
                      width="30"
                      height="30"
                    />
                    <img
                      class="block hover:scale-125 ease-in duration-300 cursor-pointer"
                      src="~/assets/images/good.gif"
                      width="30"
                      height="30"
                    />
                    <img
                      class="block hover:scale-125 ease-in duration-300 cursor-pointer"
                      src="~/assets/images/natural.gif"
                      width="30"
                      height="30"
                    />
                    <img
                      class="block hover:scale-125 ease-in duration-300 cursor-pointer"
                      src="~/assets/images/disappointed.gif"
                      width="30"
                      height="30"
                    />
                    <img
                      class="block hover:scale-125 ease-in duration-300 cursor-pointer"
                      src="~/assets/images/hate.gif"
                      width="30"
                      height="30"
                    />
                  </div>
                </div>

                <el-button icon="el-icon-chat-line-square" size="mini"
                  >Comment</el-button
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="bottom-siderbar h-12 flex items-center justify-between bg-white border-t-2 border-gray-300 border-solid"
    >
      <NuxtLink to="/create-new" class="flex-1 text-center">
        <button
          class="hover:bg-orange-primary hover:text-white hover:font-bold ease-in duration-200 py-1 px-2 rounded-xl transition-colors tra"
        >
          <i class="el-icon-circle-plus"></i>
          <span>投稿画面</span>
        </button>
      </NuxtLink>
      <NuxtLink to="/" class="flex-1 text-center">
        <button
          class="bg-orange-primary text-white font-bold ease-in duration-200 py-1 px-2 rounded-xl"
        >
          <i class="el-icon-s-shop"></i>
          <span>TOP画面</span>
        </button>
      </NuxtLink>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'HomePage',

  components: {},

  data() {
    return {
      search: {
        status: false,
        params: '',
      },
      stat: {
        rate: 5,
      },

      list_reaction: {
        good_icon: 2,
        natural_icon: 2,
        disappointed_icon: 2,
        hate_icon: 2,
      },
    };
  },

  mounted() {
    this.testFunction();
  },
  methods: {
    async testFunction() {
      const snapshot = await this.$fire.firestore.collection('hello').get();
      console.log(snapshot.docs.map((doc: any) => doc.data()));
    },
  },
});
</script>

<style lang="scss">
.el-carousel__arrow {
  background: black;
}
</style>
