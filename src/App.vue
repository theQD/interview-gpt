<template>
  <div>
    <nav>
      <div class="LOGO">复试模拟</div>

    </nav>
    <LogIn/>
  </div>
  
</template>

<script>
import LogIn from '/src/views/LogIn';
export default {
  components:{
    LogIn,

  }
    
};


</script>

<style>
*{
  margin:0;
  padding:0;
}
#app {
  height:100vh;
  background: linear-gradient(0.45turn, #3f87a6, #ebf8e1, #f69d3c);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

nav {
  padding: 30px;

  height:30px;
  display: flex;
  justify-content: flex-start;
  align-items: center;

}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.LOGO{
  font-size: 30px;
  font-family: '黑体';
  font-weight: bold;
  left:30px;
  color:black;
}
</style>
