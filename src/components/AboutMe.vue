<template>
    <div class="about-me">About Me</div>
</template>


<script>
export default {
  name: 'AboutMe',
}
</script>


<style scoped lang="scss">
@import '../style/variables';
@import '../style/generals';

.about-me {
  background-color: $second-color;
  width: calc(100% - 350px);
  border-radius: 35px;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>