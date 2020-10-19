<template>
<div>
  <h2>{{title}}</h2>
  <ul>
    <li v-for="post in posts" :key="post">
      {{post}}
    </li>
  </ul>

</div>
</template>

<script>
export default {
  name: 'Post',
  props: {
    title: String
  },
  data(){
    return {
      posts: [

          {
            "post_title": "Third Post",
            "pub_date": "2020-07-10T14:30:00Z",
            "post_content": "This is the Third post",
            "is_published": true
          },
          {
            "post_title": "First Post",
            "pub_date": "2020-07-10T13:30:00Z",
            "post_content": "This is the first post",
            "is_published": true
          }
    ]
  }
  },
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
</style>
