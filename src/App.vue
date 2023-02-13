<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <Card />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Card from "./components/Card.vue"

export default {
  name: "app",
	components: {
      Card, // <=> YourComponent: 'YourComponent'
      HelloWorld
    }	
  };
// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
