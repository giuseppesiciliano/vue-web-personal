<template>
    <div class="container">
      <MainDisplay ref="MainDisplay" />
      <ButtonsDisplay @button-click="ciao" />
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
  },
  methods: {
    ciao(screen) {
      this.$refs.MainDisplay.showScreen(screen);
    },
  }
}
</script>


<style scoped lang="scss">
.container {
  display: flex;

  width: 1350px;
  min-width: 500px;
  min-height: 80%;
  margin-left: 90px;
  margin-right: 20px;
}


@media (max-width: 1223px) {

  .container {
    margin: 0;
    width: 100%;
    height: 100%;
  }
}
</style>