<template>
  <div id="app">
    <div class="layer">
      <Container />
    </div>
    
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
  background-image: url("@/assets/sfondo.JPG");
}

.layer {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  backdrop-filter: blur(5px);
  background-color: rgba(255, 255, 255, 0.1);
}

@media (max-width: 1023px) {}
</style>
