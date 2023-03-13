<template>
  <div class="about">
    <div class="container">
      <h1>注册用户</h1>
      <form >
          <label for="username">用户名</label>
          <input type="text" id="username" name="username" palceholder="用户名" v-model="username"  required>
          <label for="username">邮箱</label>
          <input type="text" id="email" name="email" palceholder="邮箱" v-model="email" required>
          <label for="password">密码:</label>
          <input type="password" id="password" name="password" palceholder="密码" v-model="password" required >
          <label for="password">重复密码:</label>
          <input type="password" id="cpassword" name="cpassword" palceholder="密码" v-model="cpassword" required >
          <button type="submit"  @click.prevent="register">Login</button>

          
      </form>
  </div>
  </div>
</template>
<script>
import axios from 'axios';
import bcrypt from 'bcryptjs';

export default {
  data(){
    return{
      username:'',
      email:'',
      password:'',
      cpassword:''
    };
  },
  methods:{
    register: async function(){
      if(this.password !== this.cpassword){
        alert('两次输入的密码不一致');
      }
      else{
        const salt = await bcrypt.genSalt(10);
        const hashedPassword = await bcrypt.hash(this.password, salt);
        let url = 'http://localhost:3000/users';
        await axios.post(url, {
          username: this.username,
          email: this.email,
          password: hashedPassword,
        })
          .then(res => alert('注册成功'))
          .catch(err => alert('发现错误'+err));

      }
    }
  }


};


</script>
<style>
label{
  display: inline-block;
}
.about{
  display: relative;
}
.container {
  position: absolute;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  margin:auto;
  background-color: rgba(170, 168, 168, 0.185);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  padding: 20px;
  width: 60vh;
  height: 60vh;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

h1 {
  color: rgb(255, 255, 255);
}

form {
  display: flex;
  align-items: center;
  flex-direction: column;
  margin-top: 20px;
}

label {
  color: rgb(0, 0, 0);
  margin-bottom: 20px;
  text-align: left;
}

input[type="text"], input[type="password"] {
  border-radius: 5px;
  padding: 5px;
  height: 30px;
  width: 400px;
  margin-bottom: 30px;
  border: none;
  outline: none;
}

button {
  background-color: #E9C46A;
  border: none;
  border-radius: 5px;
  color: white;
  cursor: pointer;
  font-size: 16px;
  padding: 10px;
  margin-top: 20px;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #F4A261;
}

</style>
