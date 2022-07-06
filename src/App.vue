<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <MyButton msg="Test,Test,Test,Test,Test，Test"/>
  <Users></Users>
<!--  <componentA title="Hello"> Hello World</componentA>-->
  <div id="post-a">
    <componentA>Hello</componentA>
  </div>
<!--  <PostVue title="Hello World">Hello</PostVue>-->
</template>

<script>


import HelloWorld from './components/HelloWorld.vue'
import Users from "@/components/Users";
import componentA from "@/components/PostVue";

export default {
  name: 'App',
  components: {
    HelloWorld,
    Users,
    componentA
  }
}
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
