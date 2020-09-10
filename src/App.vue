<template>
  <div id="app">
    <p>
      Crossroads and
      <span class="text-interactive">
        <span class="underline"></span>
        <span>niggas</span>
      </span> be wylin'
    </p>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.text-interactive {
  position: relative;
  display: inline-block;
  z-index: 200;
  cursor: pointer;
}
.text-interactive .underline {
  display: inline-block;
  position: absolute;
  background: rgba(45, 56, 201, 0.3);
  width: 100%;
  height: 4px;
  bottom: -8px;
  left: 0;
  z-index: 20;
}
.text-interactive span:not(.underline) {
  z-index: 20000;
}
.text-interactive:hover .underline {
  height: 30px;
}
.underline {
  transition: all 300ms;
}
</style>
