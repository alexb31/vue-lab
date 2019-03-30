<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    <Dogs/>
    <Bind/>
    <Hours/>
    <Loop/>
    <Timer/>
    <Show/>
    <TwoWayBind/>
    <Methods/>
    <This/>
    <Computed/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Dogs from "./components/Dogs";
import Bind from "./components/bind";
import Hours from "./components/Hours";
import Loop from "./components/Loop";
import Timer from "./components/Timer";
import Show from "./components/Show";
import TwoWayBind from "./components/twoWayBind";
import Methods from "./components/Methods";
import This from "./components/this";
import Computed from "./components/computed";

export default {
  name: "App",
  components: {
    HelloWorld,
    Dogs,
    Bind,
    Hours,
    Loop,
    Timer,
    Show,
    TwoWayBind,
    Methods,
    This,
    Computed
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
</style>
