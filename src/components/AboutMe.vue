<template>
    <div class="about-me">
      <div class="text">
        Su di me

      </div>
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








// animazione all'apertura
.text {
  padding: 40px;
  opacity: 0;
  animation: appear 0.5s linear 0.5s forwards;
}
@keyframes appear {
  100% {
    opacity: 1;
  }
}







@media (max-width: 1223px) {

  .about-me {
    width: 100%;
  }
}
</style>