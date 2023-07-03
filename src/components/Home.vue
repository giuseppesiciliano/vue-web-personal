<template>
    <div class="home">
      <div class="text">Home</div>
    </div>
</template>


<script>
export default {
  name: 'HomeX',
}
</script>


<style scoped lang="scss">
@import '../style/variables';
@import '../style/generals';

.home {
  background-color: $second-color;
  min-width: calc(100% - 350px);
  // width: 1150px;
  border-radius: 35px;

  display: flex;
  justify-content: center;
  align-items: center;
}

.text {
  opacity: 0;
  animation: appear 0.5s linear 0.3s forwards;
}
@keyframes appear {
  100% {
    opacity: 1;
  }
}








@media (max-width: 1023px) {

  .home {
    width: 100%;
  }
}
</style>