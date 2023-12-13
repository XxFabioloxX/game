<script>

export default {
  name: 'App',
  data() {
    return {
      score: 0,
      score_one: 0,
      score_two:0,
      score_three: 0,
      random: 0,
      items:[0,0,0,0,0,0,0,0,0],
      
    }
  },
  methods: {
    lancer() {
      this.random = Math.ceil(Math.random() * 6)
      console.log(this.items)
    },
    afficherValeur(item,index){      
      this.items[index] = this.random;
      this.score = this.score_one
      this.score_one = this.items[0] + this.items[3] +this.item[6]
      // this.score+=this.items[index]
      console.log(this.items[0])

    }
  }
}
</script>

<template>
  <div class="plateau">
  <div class="case" v-for="(item, index) in items" :key="index" @click="afficherValeur(item,index)">{{ item }}</div>
  </div>
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
  position: absolute;
  right: 50%;
  width: 45px;
  height: 45px;
}

.plateau{
display: grid;
grid-template-columns: 100px 100px 100px;
  background-color: red;
  height: 300px;
  width: 300px;
}.case{

  width: 100px;
  height: 100px;
  border: 1px solid;
  border-color: black;
}
</style>
