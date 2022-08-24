<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
/*import fetch from 'fetch';

fetch('https://github.com/passor53')
  .then((data) => data.json())
  .then((user) => {
    console.log(user);
  });
  */
/*axios.get('http://localhost:8080/')
  .then((reponse) => {
    console.log(reponse.data);
  });
*/
/*axios.post('https://www.site.com', { age: 30 })
  .then((reponse) => {
    console.log(reponse.data);
  });
*/
export default {
  name: 'HelloWorld',
  props: {
    msg: String
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
