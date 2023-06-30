<template>
  <div id="app">
    <Container />

    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Container from './components/Container.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Container,
  }
}
</script>

<style lang="scss">
@import './style/variables';
@import './style/generals';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;

  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

</style>
