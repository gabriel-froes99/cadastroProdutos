<script setup>
import cadastroProduto from './components/cadastroProduto.vue';
</script>

<template>
  <cadastroProduto msg="cadastro Produto"/>
</template>

<style>
body {
  margin: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-image: linear-gradient(to bottom right, #3f3f3f, #6c6a6a);
  background-attachment: fixed;
  min-height: 100vh;
  color: #f0f0f0;
}

#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  text-align: center;
}
</style>
