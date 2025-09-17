<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Step002View/>
  <Step003view/>
  <Step004View/>
  <Step005View/>
  <Step006View/>
  <Step007View/>
  <Step008View/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Step002View from "./components/step002view.vue";
import Step003view from "@/components/step003view.vue";
import Step004View from "@/components/step004view.vue";
import Step005View from "@/components/Step005View.vue";
import Step006View from "@/components/Step006View.vue";
import Step007View from "@/components/Step007View.vue";
import Step008View from "@/components/Step008View.vue";

export default {
  name: 'App',
  components: {
    Step008View,
    Step007View,
    Step006View,
    Step005View,
    Step004View,
    Step002View,
    Step003view,
    HelloWorld
  }
}
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
