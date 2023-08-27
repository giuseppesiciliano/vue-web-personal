<template>
    <div class="contact">
      <div class="text">Contatti</div>
    </div>
</template>


<script>
export default {
  name: 'ContactX',
}
</script>


<style scoped lang="scss">
@import '../style/variables';
@import '../style/generals';

.contact {
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
  animation: appear 0.5s linear 0.5s forwards;
}

@keyframes appear {
  100% {
    opacity: 1;
  }
}




@media (max-width: 1223px) {

  .contact {
    width: 100%;
  }
}
</style>