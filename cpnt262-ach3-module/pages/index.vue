<script setup>
const colorMode = useColorMode()
</script>

<template>
  <h1>ColorMode Module</h1>
  <p>To see the changes, please change to light to dark theme in the browser or from dark to light.</p>
</template>

<style>
body {
  background-color: #fff;
  color: rgba(0,0,0,0.8);
}
.dark-mode body {
  background-color: #091a28;
  color: #ebf4f1;
}
.sepia-mode body {
  background-color: #f1e7d0;
  color: #433422;
}
</style>