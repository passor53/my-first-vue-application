<template>
  <img src="./assets/Logo_Morpion.png" alt="Logo_morpion">
  <HelloWorld msg="Ça gratte, mais ça se joue aussi ! " />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
  }
}

</script>

<style>
body {
  text-align: center;
  background-image: url('./assets/Fond-ecran.jpg');
  background-repeat: no-repeat;
  background-size: 100vw 100vh;
}

.rdj {
  position: relative;
  border: solid 1px gray;
  border-radius: 1vw;
  margin: 0 45vw 0 45vw;
  color: orange;
  background-color: rgb(48, 47, 47);
}

.regles {
  position: absolute;
  transition: opacity .5s;
  opacity: 0;
  top: 25vh;
  left: 15vw;
  border: solid 2px whitesmoke;
  border-style: outset;
  border-radius: 3vw;
  background-color: rgb(48, 47, 47);
  color: orange;
  text-align: center;
  width: 70vw;
}

.regles:hover {
  opacity: 90;
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #030302;
  margin-top: 60px;
}

.case {
  border: 3px outset gray;
  background-color: rgb(245, 245, 245);

  height: 100px;
  line-height: 100px;
  font-size: 60px;
}

#jeu {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  width: 300px;
  margin: auto;
}

.hello {
  color: rgb(0, 0, 32);
}

.players {
  display: flex;
  flex-direction: row;
  justify-content: center;

  margin: 0 18vw 0 18vw;
}

.titre2 {
  border: solid 1px gray;
  background-color: rgb(48, 47, 47);
  border-radius: 5vw;
  margin: 0 5vw 0 5vw;
  margin-top: 10vh;
  color: orange;
}

.label {
  color: orange;
  border: solid 1px gray;
  background-color: rgb(48, 47, 47);
  border-radius: 2vw;
  padding: 0 1vw 0 1vw;
}

.joueur1 {
  background-image: url(./assets/blaster.png);
  background-size: 27vw;
  background-repeat: no-repeat;
  width: 50vw;
  height: auto;
  border-radius: 5vh;
  height: 40vh;
  background-position: center;
  margin-right: 5vw;
  margin-left: -5vw;
}


.joueur2 {
  background-image: url(./assets/blaster.png);
  background-size: 27vw;
  background-repeat: no-repeat;
  width: 50vw;
  height: auto;
  border-radius: 5vh;
  height: 40vh;
  background-position: center;
  margin-left: 5vw;
  margin-right: -5vw;
}

.envoyer {
  margin: 16.5vh 0 16.5vh 0;
  border-radius: 5vw;
  border-color: gray;
  border-style: solid;
  background-color: rgb(48, 47, 47);
  color: orange;
}

.affichage_joueur {
  text-transform: uppercase;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: orange;
  border: solid 1px gray;
  background-color: rgb(48, 47, 47);
}

.rejouer {
  justify-self: center;
  align-self: center;
  border: solid 1px gray;
  border-radius: 4vw;
  background-image: url(./assets/refresh.png);
  background-color: rgb(48, 47, 47);
  background-size: 5vw 5vh;
  background-repeat: no-repeat;
  margin-top: 2vh;
  color: orange;
  padding: 0 5vw 3vh 0;
  cursor: pointer;
  text-decoration: solid;

}
</style>
