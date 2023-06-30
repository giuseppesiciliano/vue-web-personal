<template>
    <div class="home">Home</div>
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
  width: calc(100% - 350px);
  border-radius: 35px;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>