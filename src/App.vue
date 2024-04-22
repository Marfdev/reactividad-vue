<script setup>
import HelloWorld from './components/HelloWorld.vue'
import ReactiveHelloWorld from './components/ReactiveHelloWorld.vue';
import AgeCalculator from './components/AgeCalculator.vue';
import WatchCounter from './components/WatchCounter.vue';
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <H1> REFS </H1>
  <HelloWorld/>
  <H1> REACTIVE </H1>
  <ReactiveHelloWorld/>
  <h1> COMPUTED</h1>
  <AgeCalculator/>
  <h1> WATCH </h1>
  <WatchCounter/>


</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
