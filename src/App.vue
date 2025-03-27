<template>
  <the-form></the-form>
</template>

<script>
import TheForm from './components/TheForm.vue';

export default {
  components: {
    TheForm
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  height: 100vh;
  margin: 0;
  background: linear-gradient(180deg, rgba(14, 0, 255, 1) 0%, rgba(0, 0, 105, 1) 50%, rgba(0, 214, 255, 1) 100%);
}
</style>