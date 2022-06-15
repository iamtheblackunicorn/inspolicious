<template>
  <ul>
   <li v-for="word in randWords" v-bind:key="word.msg">
    {{ word.msg }}
   </li>
  </ul>
</template>

<script>
export default {
  name: 'RandWordContainer',
  props: ['randWords']
}
</script>