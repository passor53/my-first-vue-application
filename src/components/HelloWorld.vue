<template>
  <div class="bloc_page">
    <p class="rdj" v-if="table == undefined">Règles</p>
    <p class="regles" v-if="table == undefined">
      <br>RÈGLE DU JEU <br><br>
      - Jeu qui se joue à deux joueurs, sur un damier de 3 cases par 3 cases.<br />
      - Chaque joueur est représenté par un "symbole".<br />
      - Un joueur utilise toujours le même type de "symbole".<br />
      - Un premier joueur dessine son symbole sur une case,<br /> puis c'est au tour de l'autre joueur de dessiner
      son
      symbole
      sur une case vide.<br />
      - Le but du jeu est de réussir à aligner ses trois symboles (horizontal, vertical ou diagonale), on remporte
      alors
      la partie.<br><br>
    </p>
    <div class="hello">
      <h1>{{  msg  }}</h1>
    </div>

    <div id="jeu" v-if="table != undefined">
      <div v-for="i in 9" :key="i" :data-value=i v-on:click="cycle_jeu($event)" class="case"></div>

      <p class="affichage_joueur">{{  this.pseudo1  }} : {{  this.jeton1  }}</p>
      <input class="rejouer" type="button" title="Rejouer" onclick='window.location.reload(false)' />
      <p class="affichage_joueur">{{  this.pseudo2  }} : {{  this.jeton2  }}</p>
    </div>

    <div class="players" v-if="table == undefined">

      <div class="joueur1">
        <h2 class="titre2">Joueur 1</h2>
        <h4>
          <label class="label" for="pseudo1">Pseudo :</label>
          <input type="text" name="pseudo" id="pseudo1" maxlength="8" />
        </h4>
        <select name="jeton1" id="jeton1">
          <option value="X">X</option>
          <option value="O">O</option>
        </select>
      </div>
      <input class="envoyer" type="button" value="Jouer" v-on:click="send" />

      <div class="joueur2">
        <h2 class="titre2">Joueur 2</h2>
        <h4>
          <label class="label" for="pseudo2">Pseudo :</label>
          <input type="text" name="pseudo" id="pseudo2" maxlength="8" />
        </h4>
        <select name="jeton2" id="jeton2">
          <option value="X">X</option>
          <option value="O">O</option>
        </select>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

  data() {
    return {
      table: undefined,
      pseudo1: '',
      pseudo2: '',
      jeton1: '',
      jeton2: '',
      tourjeu: 1,
    }

  },


  methods: {
    send() {
      this.pseudo1 = document.getElementById('pseudo1').value;
      this.table = true;
      console.log(this.pseudo1)

      this.jeton1 = document.getElementById('jeton1').value;
      console.log(this.jeton1)

      this.pseudo2 = document.getElementById('pseudo2').value;
      this.table = true;
      console.log(this.pseudo2)

      this.jeton2 = document.getElementById('jeton2').value;
      console.log(this.jeton2)
    },


    cycle_jeu(event) {

      if (this.tourjeu % 2 == 1) { event.target.innerHTML = this.jeton1; }
      if (this.tourjeu % 2 == 0) { event.target.innerHTML = this.jeton2; }

      let val = event.target.getAttribute('data-value');
      console.log(val);

      this.tourjeu = this.tourjeu + 1;
      this.table.find(val == val)
      val = Array.splice(val, 1, 'X') // et je suis bloqué ici pour le moment !!!
    }
  }

}

</script>

<style scoped>
</style>