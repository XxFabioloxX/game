<script>

export default {
  name: 'App',
  data() {
    return {
      score: 0,
      random: 0,
      items:[0,0,0,0,0,0,0,0,0],
      caseJeu: 0
    }
  },
  methods: {
    lancer() {
      this.random = Math.ceil(Math.random() * 6)
      console.log(this.random)
      // this.game = this.random
      // console.log(this.game)
    },

    afficherValeur(item,index){
      
      this.items[index] = this.random; 
    
    }


  }
}
</script>

<template>
  <div v-for="(item, index) in items" :key="index" @click="afficherValeur(item,index)">{{ item }}</div>

  <div class="score">{{ score }}</div>

  <div class="de">
    <button @click="lancer">{{ random }}</button>
  </div>
</template>

<style scoped>
.col {
  border: 2px solid;
  border-color: black;
  width: 90px;
  height: 90px;
  text-align: center center;
}

button {
  width: 45px;
  height: 45px;
}
</style>
