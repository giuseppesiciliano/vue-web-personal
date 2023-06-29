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
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;

  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

</style>
