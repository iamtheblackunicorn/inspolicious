<!--
Inspolicious by Alexander Abraham,
a.k.a. "The Black Unicorn", a.k.a. "Angeldust Duke".
Licensed under the MIT license.
-->

<template>
  <!--A component for the footer text.-->
  <footer>
   {{ creditsText }}
  </footer>
</template>

<script>
// Exporting the field "creditsText"
// for use in "App.vue"
export default {
  name: 'FooterText',
  props: ['creditsText']
}
</script>