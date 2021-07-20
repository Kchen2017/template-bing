<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
import { getList } from './api/index';

export default {
  name: 'App',
  mounted() {
    getList({
      // get请求放params
      // post请求放data里面
      // 参考链接：https://axios-http.com/docs/req_config
      params: {
        sss: '3',
      },
    });
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
