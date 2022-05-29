<template>
  <div class="bg-phone">
    <div id="login-page" class="flex flex-col h-full pb-5 px-3">
      <div class="login__header mb-10">
        <p class="font-semibold text-4xl">Login</p>
      </div>
      <div class="login__content flex-1">
        <el-form label-position="top" :model="form">
          <el-form-item :label="$t('login.form.email')">
            <el-input
              v-model="form.user_name"
              type="email"
              :placeholder="$t('login.placeholder.email')"
            ></el-input>
          </el-form-item>
          <el-form-item :label="$t('login.form.password')">
            <el-input
              v-model="form.password"
              type="password"
              :placeholder="$t('login.placeholder.password')"
            ></el-input>
          </el-form-item>
        </el-form>
      </div>
      <div class="login__footer text-center">
        <el-button type="primary" class="w-full cursor-pointer" round
          >Sign in</el-button
        >
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

const initialForm = () => ({
  user_name: '',
  password: '',
});

export default Vue.extend({
  name: 'LoginPage',
  data() {
    return {
      form: initialForm(),
      checked_save_account: false,
    };
  },
});
</script>
