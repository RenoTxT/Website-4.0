<script>
export default {
  name: 'App',
  data(){
    return{
      bubbleClass: 'bubble',
      containerClass: 'container',
      contentClass: 'content',
    }
  }
}
</script>
``
<template>
  <div :class="containerClass">
    <div :class="bubbleClass">
      <span style="--i:11"></span>
      <span style="--i:12"></span>
      <span style="--i:24"></span>
      <span style="--i:10"></span>
      <span style="--i:14"></span>
      <span style="--i:23"></span>
      <span style="--i:18"></span>
      <span style="--i:16"></span>
      <span style="--i:19"></span>
      <span style="--i:20"></span>
      <span style="--i:22"></span>
      <span style="--i:25"></span>
      <span style="--i:18"></span>
      <span style="--i:21"></span>
      <span style="--i:15"></span>
      <span style="--i:13"></span>
      <span style="--i:26"></span>
      <span style="--i:17"></span>
      <span style="--i:13"></span>
      <span style="--i:28"></span>
      <span style="--i:11"></span>
      <span style="--i:12"></span>
      <span style="--i:24"></span>
      <span style="--i:10"></span>
      <span style="--i:14"></span>
      <span style="--i:23"></span>
      <span style="--i:18"></span>
      <span style="--i:16"></span>
      <span style="--i:19"></span>
      <span style="--i:20"></span>
      <span style="--i:22"></span>
      <span style="--i:25"></span>
      <span style="--i:18"></span>
      <span style="--i:21"></span>
      <span style="--i:15"></span>
      <span style="--i:13"></span>
      <span style="--i:26"></span>
      <span style="--i:17"></span>
      <span style="--i:13"></span>
      <span style="--i:28"></span>
    </div>
    <div :class="contentClass">
      <h1>Hello World</h1>
    </div>
  </div>
</template>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  min-height: 100vh;
  background: #0c192c;
}
.container{
  position: relative; 
  width: 100%;
  height: 100vh;
  overflow: hidden;
}
.bubble{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  flex-wrap: wrap;
  pointer-events: none; /* Prevents interaction with the bubbles */
  z-index: 0; /* Places bubbles behind main content */
}
.bubble span{
  position: relative;
  width: 30px;
  height: 30px;
  background: #4fc3dc;
  margin: 0 4px;
  border-radius: 50%;
  box-shadow: 0 0 0 10px #4fc3dc44,
  0 0 50px #4fc3dc,
  0 0 100px #4fc3dc;
  animation: animate 15s linear infinite;
  animation-duration: calc(125s/var(--i));
}
.bubble span:nth-child(even){
  background: #ff2d75;
  box-shadow: 0 0 0 10px #ff2d7544,
  0 0 50px #ff2d75dc,
  0 0 100px #ff2d75dc;
}
@keyframes animate{
  0%{
    transform: translateY(100vh) scale(0);
  }
  100%{
    transform: translateY(-10vh) scale(1);
  }
}
.content {
  position: relative;
  z-index: 1; /* Places the main content above the bubbles */
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  color: white; /* Ensures text is visible */
}

</style>
