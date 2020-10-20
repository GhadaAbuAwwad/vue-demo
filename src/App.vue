<template>
  <div id="app">
    <img alt="Vue logo" src="@/assets/pic1.jpg" width="300" height="300">
    <h1>Latest Posts from  our Blog</h1>
    <Post title="Here I display latest blog's posts"></Post>
    <h1>All Polls</h1>
    <Polls title="Here I display All Polls"></Polls>
  </div>
</template>

<script>
import Post from "@/components/Post";
import Polls from "@/components/Polls";

export default {
  name: 'App',
  components: {
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
