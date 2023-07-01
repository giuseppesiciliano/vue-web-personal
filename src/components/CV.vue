<template>
    <div class="cv">
      <div class="text">Curriculum Vitae</div>
    </div>
</template>


<script>
export default {
  name: 'CV',
}
</script>


<style scoped lang="scss">
@import '../style/variables';
@import '../style/generals';

.cv {
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
</style>