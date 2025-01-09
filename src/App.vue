<script>
import Calculadora from "./components/Calculadora.vue";

export default {
  name: "App",
  components: {
    Calculadora,
  },
};
</script>

<template>
  <div id="app">
    <Calculadora />
  </div>
</template>

<style>
body {
  background-color: #e0e0e0;
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}
</style>
