<template>
    <div class="about-me">
      <div class="text">About Me</div>
    </div>
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

.text {
  opacity: 0;
  animation: appear 0.5s linear 0.5s forwards;
}

@keyframes appear {
  100% {
    opacity: 1;
  }
}
</style>