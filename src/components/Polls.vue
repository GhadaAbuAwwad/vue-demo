<template>
  <div>
    <h2>{{title}}</h2>
    <ul>
      <li>
        <div>Lorem ipsum dolor sit amet, consectetur.</div>
        <div>At culpa deleniti deserunt facilis sit.</div>
        <div>Adipisci aperiam consequatur non vitae voluptatibus.</div>
        <div>Animi expedita natus obcaecati perferendis sed.</div>
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'Polls',
  props: {
    title: String
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
</style>
