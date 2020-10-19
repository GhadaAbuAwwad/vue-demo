<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <h1>Latest Posts from  our Blog</h1>
    <Post title="Here I display latest blog's posts"></Post>
    <h1>All Polls</h1>
    <Polls title="Here I display All Polls"></Polls>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Post from "@/components/Post";
import Polls from "@/components/Polls";

export default {
  name: 'App',
  components: {
    HelloWorld,
    Post,
    Polls
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
