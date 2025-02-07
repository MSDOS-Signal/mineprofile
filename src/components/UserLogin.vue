<template>
  <div class="login-container">
    <div class="logo">
      <img :src="logoSrc" alt="Vue Logo" onclick="alert('本网站用vue框架制作')"/>
    </div>
    <h1>登录</h1>
    <form @submit.prevent="handleLogin">
      <div class="form-group">
        <label for="username">用户名</label>
        <input type="text" id="username" v-model="username" required />
      </div>
      <div class="form-group">
        <label for="password">密码</label>
        <div class="password-container">
          <input
            :type="isPasswordVisible ? 'text' : 'password'"
            id="password"
            v-model="password"
            required
          />
          <button type="button" @click="togglePasswordVisibility" class="toggle-password">
            {{ isPasswordVisible ? '👁️' : '👁️‍🗨️' }}
          </button>
        </div>
      </div>
      <button type="submit" class="btn">登录</button>&nbsp;
      <button class="btn1" type="submit" onclick="alert('联系微信DXH08060927获取用户名和密码')">获取用户名/密码</button>
    </form>
   
  </div>
  
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: '',
      logoSrc: require('@/assets/vue-logo.png'), // 确保将 Vue logo 放在 assets 目录
      isPasswordVisible: false, // 密码可见性状态
    };
  },
  methods: {
    handleLogin() {
      // 登录逻辑
      if (this.username === atob(atob(atob('WTIwNWRtUkJQVDA9'))) && this.password === atob(atob(atob('WlVkc2RXRkhSblpOYWtGM1RtYzlQUT09')))) {
        // 登录成功，跳转到 index2.html
        window.location.href = 'index2.html';
      } else {
        alert('用户名或密码错误！');
      }
    },
    togglePasswordVisibility() {
      this.isPasswordVisible = !this.isPasswordVisible; // 切换密码可见性
    },
  },
};
</script>

<style scoped>
body{
  background: linear-gradient(135deg, #6a4dc0, #619e64);
  text-shadow: 0 0 10px #f2eeee;
}
.login-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 90vh;
  background: linear-gradient(135deg, #6a4dc0, #619e64);
  color: white;
  font-family: Arial, sans-serif;
  position: relative;
}

.logo img {
  width: 100px;
  height: auto;
  text-shadow: 0 0 10px #a1e1a4;
  animation: logo-animation 0.4s infinite alternate;
}

h1 {
  margin: 20px 0;
  font-size: 2em;
  text-shadow: 0 0 10px #ebeaea;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
  font-size: 20px;
  font-weight: bold;
  text-shadow: 0 0 10px #fffefe;
}

.password-container {
  position: relative;
}

input {
  padding: 10px;
  border: none;
  border: #000 solid;
  border-radius: 5px;
  width: 300px;
  transition: all 0.5s;
  box-shadow: 0 0 10px #fff;
}
input:hover{
  border: 2px solid #55fc82;
}
.btn {
  width: 155px;
  padding: 10px 20px;
  background-color: #000;
  color: #fff;
  border: none;
  font-weight: bold;
  box-shadow: 0 0 10px #093e58;
  text-shadow: 0 0 10px #fff;
  font-size: 15px;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s;
}
.btn1 {
  width: 160px;
  padding: 10px 20px;
  background-color: #000;
  box-shadow: 0 0 10px #093e58;
  color: #fff;
  border: none;
  text-shadow: 0 0 10px #fff;
  font-weight: bold;
  font-size: 15px;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s;
}


button:hover {
  background-color: #c8e6c9;
  text-shadow: 0 0 10px #70d592;
  color: #000;
}

.toggle-password {
  position: absolute;
  right: 10px;
  top: 50%;
  transform: translateY(-50%);
  background: none;
  border: none;
  color: white;
  cursor: pointer;
}

/* 添加放大动画 */
@keyframes logo-animation {
  0% {
    transform: scale(1.8);
  }
  100% {
    transform: scale(1.1);
  }
}

</style>
