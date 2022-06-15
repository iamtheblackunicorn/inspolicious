<!--
Inspolicious by Alexander Abraham,
a.k.a. "The Black Unicorn", a.k.a. "Angeldust Duke".
Licensed under the MIT license.
-->

<template>
  <!--A component for static text.-->
  <h1>{{ name }}</h1>
  <p>{{ instructions }}</p>
</template>

<script>
// Exporting the fields "name" and "instructions"
// for use in "App.vue"
export default {
  name: 'HeadingText',
  props: ['name', 'instructions']
}
</script>