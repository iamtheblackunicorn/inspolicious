<template>
  <RandWordContainer :randWords="words.randWords"/>
  <button @click="reset()">REROLL</button>
</template>

<script>

import RandWordContainer from './components/RandWordContainer.vue'

export default {

  name: 'App',
  components: {
    RandWordContainer
  },

  data(){
    var randomWords = require('random-words');
    return {
      words: {
        randWords: randomWords(5).join(' ')
      }
    }
  },

  methods: {

    reset(){
      var randomWords = require('random-words');
      var viewModel = this;
      viewModel.words.randWords = randomWords(5).join(' ');
    }

  }  
}
</script>