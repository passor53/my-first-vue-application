<template>
  <img alt="Vue logo" src="./assets/Logo_Morpion.png">
  <HelloWorld msg="Un jeu qui gratte un peu et qui comporte des règles:" />
  <input type="button" value="Entrer" />
</template>

<script>
/*let xhr = new XMLHttpRequest();
xhr.onreadystatechange = () => {
  if (xhr.readyState === 4 && xhr.status === 200) {
    console.log(JSON.parse(xhr.response));
  }
};
xhr.open('GET', 'https://api.github.com/users/passor53');
xhr.send(null); */

import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
