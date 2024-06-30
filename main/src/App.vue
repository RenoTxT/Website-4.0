<script>
export default {
  name: 'App',
  data(){
    return{
      logoClass: 'logo',
    }
  }
}
</script>
``
<template>
  <nav>
    <div :class="logoClass">
      <img src="./assets/krios.png">
    </div>
    <ul>
      <li>Home</li>
    </ul>
  </nav>
  <body>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </body>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Courier New', Courier, monospace;
  transition: .5s;
}

body{
  background-color: #0d0d0d;
}

body p{
  color: #f2f2f2;
}

nav{
  display: flex;
  justify-content: space-between; 
  background: #f2f2f2;
  width: 100%;
  height: 80px;
}

.logo{
  line-height: 80px;
  padding: 0px 100px;
}

.logo img{
  max-height: 50px;
  margin-top: 10px;
}

nav ul{
  float: right;
  margin-right: 20px;
}

nav ul li{
  display: inline-block;
  margin-top: 25px;
  font-size: 16px;
  border-radius: 3px;
  transition: .5s;
  padding: 7px 13px;
}
</style>
