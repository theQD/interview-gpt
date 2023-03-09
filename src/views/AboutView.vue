<template>
  <div class="about">
    <div class="container">
      <h1>Login</h1>
      <form>
          <label for="username">用户名</label>
          <input type="text" id="username" name="username" required>

          <label for="password">Password:</label>
          <input type="password" id="password" name="password" required>

          <button type="submit">Login</button>
          <form action=""></form>
          
      </form>
  </div>
  </div>
</template>
<style>
.container {
  background-color: rgba(170, 168, 168, 0.185);
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  padding: 20px;
  width: 500px;
  margin: auto;
  margin-top: 10%;
  text-align: center;
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
