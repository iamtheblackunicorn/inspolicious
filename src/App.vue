<template>
  <div class="content">
   <HeadingText name="Inspolicious" instructions="Get random words to inspire creative efforts and press the button to regenerate them."/>
   <br/>
   <p>Your words:</p>
   <RandWordContainer :randWords="words.randWords"/>
   <br/>
   <br/>
   <button @click="reset()">REROLL</button>
  </div>
  <br/>
</template>

<script>

import RandWordContainer from './components/RandWordContainer.vue'
import HeadingText from './components/Heading.vue'

export default {

  name: 'App',
  components: {
    RandWordContainer,
    HeadingText
  },

  data(){
    var randomWords = require('random-words');
    var wordList = [];
    var nakedWords = randomWords(5);
    for (var i = 0; i < nakedWords.length; i++) {
      const wordObj = {msg: nakedWords[i]};
      wordList.push(wordObj);
    }
    return {
      words: {
        randWords: wordList
      }
    }
  },

  methods: {

    reset(){
      var viewModel = this;
      var randomWords = require('random-words');
      var wordList = [];
      var nakedWords = randomWords(5);
      for (var i = 0; i < nakedWords.length; i++) {
        const wordObj = {msg: nakedWords[i]};
        wordList.push(wordObj);
      }
      viewModel.words.randWords = wordList;
    }

  }  
}
</script>

<style lang="scss">

@font-face {
  font-family: 'PSB';
  src: url('https://blckunicorn.art/assets/fonts/PSB.ttf') format('truetype');
}

$stdFont: 'PSB';
$bgColor: #433966;
$divColor:#BC7FFE;
$contentColor:#FFFFFF;
$gradientColorOne:#70C7FE;
$gradientColorTwo:#FF7BAC;

html,body {
  top:0;
  right:0;
  left:0;
  bottom:0;
  padding:0px;
  margin:0px;
  width:100vw;
  height:100vh;
  background-color:$bgColor;
}

h1 {
  text-align:center;
  font-family: 'PSB';
  color: $contentColor;
  font-size: 40px;
  padding: 0px;
  margin-left: 0px;
  margin-right: 0px;
  margin-top: 0px;
  margin-bottom: 10px;
}

p {
  text-align:left;
  font-family: 'PSB';
  color: $contentColor;
  font-size: 30px;
  padding: 0px;
  margin-left: 0px;
  margin-right: 0px;
  margin-top: 0px;
  margin-bottom: 10px;
}

div.content {
  background-color: $divColor;
  width: 80%;
  padding: 20px;
  margin: 0 auto;
  display: block;
  border-radius: 15px;
  margin-top: 30px !important;
  margin-bottom: 30px !important;
}

button {
  width: 100%;
  background: linear-gradient( 45deg, $gradientColorOne, $gradientColorTwo);
  border: none;
  border-radius: 15px;
  font-size: 30px;
  color: $contentColor;
  padding: 20px;
  margin: 0px;
  transition-duration: 0.6s;
  font-family: $stdFont;
}

button:hover {
  padding: 25px;
}

ul {
  width: 100%;
  margin-top: 0px;
  margin-bottom: 10px;
  margin-right: 0px;
  margin-left: 0px;
  list-style: none;
  padding: 0px;
}

li {
  width: 100%;
  padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 0px;
  padding-right: 0px;
  border-radius: 15px;
  margin-left: 0px;
  margin-right: 0px;
  margin-bottom: 10px;
  margin-top: 0px;
  text-align: center;
  border: 3px solid $contentColor;
  font-size: 28px;
  color: $contentColor;
  font-family: $stdFont;
  background-color: transparent;
}

@media screen and (max-width: 800px){
  h1 {
    font-size: 35px;
  }
  p {
    font-size: 25px;
  }
  div.content {
    width: 85%;
  }
  button {
    font-size: 25px;
    padding: 10px;
  }
  li {
    font-size: 23px;
  }
}


</style>