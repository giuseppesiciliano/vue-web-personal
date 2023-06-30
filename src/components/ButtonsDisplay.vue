<template>
    <div class="buttons-display">

        <!-- menu di navigazione -->
        <nav></nav>

        <!-- avanti / indietro -->
        <div class="next-prev"></div>
    </div>
</template>


<script>
export default {
  name: 'ButtonsDisplay',
}
</script>


<style scoped lang="scss">
@import '../style/variables';

.buttons-display {
  width: 100px;

  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

nav {
  height: 300px;
}

.next-prev {
  height: 130px;
}

nav, 
.next-prev {
  width: 70px;
  background-color: $second-color;
  border-radius: 40px;
  box-shadow: 0px 0px 500px 0px rgba(0, 0, 0, 0.1);
}
</style>