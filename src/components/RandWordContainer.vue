<!--
Inspolicious by Alexander Abraham,
a.k.a. "The Black Unicorn", a.k.a. "Angeldust Duke".
Licensed under the MIT license.
-->

<template>
  <!--A component to iterate over a bunch of random words.-->
  <ul>
   <li v-for="word in randWords" v-bind:key="word.msg">
    {{ word.msg }}
   </li>
  </ul>
</template>

<script>
// Exporting the "randWords" object array.
export default {
  name: 'RandWordContainer',
  props: ['randWords']
}
</script>