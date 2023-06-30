<template>
    <div class="container">
      <MainDisplay />
      <ButtonsDisplay />
    </div>
</template>


<script>
import MainDisplay from './MainDisplay.vue';
import ButtonsDisplay from './ButtonsDisplay.vue';

export default {
  name: 'ContainerA',
  components: {
    MainDisplay,
    ButtonsDisplay,
  }
}
</script>


<style scoped lang="scss">
.container {
  // background-color: pink;

  display: flex;

  width: 1350px;
  min-width: 500px;
  min-height: 80%;
  margin-left: 90px;
  margin-right: 20px;
}
</style>