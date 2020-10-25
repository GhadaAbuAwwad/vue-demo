<template>
<div>
  <h2>{{title}}</h2>
  <h1 class="error">{{error_msg}}</h1>
  <ul>
    <li v-for="post in posts" :key="post.id">
      {{post.post_title}}
    </li>
  </ul>

</div>
</template>

<script>
/* eslint-disable */
import axios from 'axios'
export default {
  name: 'Post',
  props: {
    title: String
  },
  data() {
    return {
      posts: [] ,
      error_msg: ''
    }
  },
  created() {
    //fetch data from api or data souce
    console.log('Fetching Data ..')
    let configs = {
      responseType: 'json'
    }
    axios.get('http://127.0.0.1:8000/blogs/post/', configs)
        .then(response=>{
          // save response data
          let server_data = response.data
          let status_code=response.status
          this.posts=server_data
          console.log('response has arrived' )
          console.log(server_data)
          console.log(status_code)
        })
    .catch(error => {
      // print error
      this.error_msg="please call Areeb"
      console.log('error happened')
    })
    console.log('Done Fetching')

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.error
{
  color:red;
}

</style>
