<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Step002View/>
  <Step003view/>
  <div class="container">
    <Step004View/>
    <Step005View/>
    <Step006View/>
    <Step007View/>
    <Step008View/>
    <Step009View/>
    <Step010View/>
    <Step011View/>
  </div>
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
import Step009View from "@/components/Step009View.vue";
import Step010View from "@/components/Step010View.vue";
import Step011View from "@/components/Step011View.vue";

export default {
  name: 'App',
  components: {
    Step011View,
    Step010View,
    Step009View,
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
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}
/* col 스타일 */
.col {
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  align-items: flex-start;
  justify-content: center;
  min-height: 150px;
  text-align: center;
  font-family: Arial, sans-serif;
}

</style>
