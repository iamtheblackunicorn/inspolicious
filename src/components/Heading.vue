<template>
  <h1>{{ name }}</h1>
  <p>{{ instructions }}</p>
</template>

<script>
export default {
  name: 'HeadingText',
  props: ['name', 'instructions']
}
</script>