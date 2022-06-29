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
        <div id="info_shop">
          <div class="shop__banner bg-white">
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
          <div class="shop__name bg-white p-2 mt-2">
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
          </div>
          <div class="shop__stat bg-white p-2 mt-2">
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

        <div class="shop__info bg-white py-2 px-4 mt-2">
          <div
            class="shop__info--row flex items-start mb-3 text-base md:text-sm"
          >
            <i class="el-icon-time mr-2 pt-1"></i>
            <span>08h00 ~ 21h00</span>
          </div>
          <div
            class="shop__info--row flex items-start mb-3 text-base md:text-sm"
          >
            <i class="el-icon-s-ticket mr-2 pt-1"></i>
            <span>25,000$ - 50,000$</span>
          </div>
          <div class="shop__info--row flex items-start text-base md:text-sm">
            <i class="el-icon-location mr-2 pt-1"></i>
            <p>
              16 Lý Thường Kiệt, Hải Châu ,Sơn Trà <br />
              <span class="text-blue-500"><u>Chỉ Đường</u></span>
            </p>
          </div>
        </div>

        <div class="shop__info2 bg-white py-2 px-4 mt-2">
          <p class="shop__info2--title text-sm text-center mb-2 font-bold">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tenetur,
            debitis.
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Repellendus, cupiditate eveniet tenetur facilis itaque aliquam?
            Veniam enim saepe sequi in expedita modi voluptatum repellendus aut
            nihil blanditiis optio quis, praesentium maxime eligendi quisquam
            sint labore. Unde placeat velit nulla modi quibusdam. Vero enim
            magnam sint similique expedita sed minus, ab repudiandae tempora
            odit iure ea fugit veritatis molestias vel. Ducimus nihil
            exercitationem ipsum illum debitis eaque officiis impedit quaerat,
            accusamus saepe excepturi sunt voluptas a sed, cum itaque vel quas
            praesentium ipsa? Ullam voluptatum sit nostrum deleniti, rerum quasi
            iusto ea perferendis nesciunt, fugit sed consectetur, iste facilis
            dolorem mollitia!
          </p>
        </div>

        <div class="shop__comment bg-white py-2 mt-2">
          <div
            class="fb-comments"
            data-href="https://developers.facebook.com/docs/plugins/comments#configurator"
            data-width="100%"
            data-numposts="5"
          ></div>
        </div>
      </div>
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
});
</script>

<style lang="scss">
.el-carousel__arrow {
  background: black;
}
</style>
