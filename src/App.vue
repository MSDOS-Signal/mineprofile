<template>
  <div id="app">
    <UserLogin />
  </div>
  
</template>

<script>
import UserLogin from './components/UserLogin.vue';


export default {
  components: {
    UserLogin,
  },
};
</script>

<style>
/* 你可以在这里添加全局样式 */
body{
  background: linear-gradient(135deg, #6a4dc0, #619e64);
}

</style>
