<template>
    <div class="main-display">

      <div class="profilo">
        <img src="../assets/img-profilo.jpeg" alt="">

        <div class="nome">Giuseppe Siciliano</div>

        <div class="professione">Web Developer</div>

        <div class="social">
            <a href=""><i class="fa-brands fa-instagram"></i></a>
            <a href=""><i class="fa-brands fa-square-facebook px-12"></i></a>
            <a href=""><i class="fa-brands fa-linkedin"></i></a>
        </div>

        <div class="cv">Download CV</div>

      </div>

      <div class="slides">slides</div>
    </div>
</template>


<script>
export default {
  name: 'MainDisplay',
}
</script>


<style scoped lang="scss">
@import '../style/variables';
@import '../style/generals';

.main-display {
  background-color: $primary-color;
  border-radius: 35px;
  box-shadow: 0px 20px 500px 10px rgba(0, 0, 0, 0.3);
  width: calc(100% - 100px);
  overflow: hidden;
  display: flex;
  color: white;
}

.profilo {
  background-color: $primary-color;
  width: 350px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  img {
    max-width: 100%;
    height: 180px;
    border-radius: 50%;
    border: 2px solid $second-color;
    margin-top: 10px;
  }

  .nome {
    font-size: 35px;
    font-weight: 800;
    margin-top: 40px;
  }

  .professione {
    font-size: 20px;
    margin: 10px 0 30px 0;
  }

  a {
    color: $second-color;
    font-size: 25px;
    margin: 0 15px;
  }

  .cv {
    margin-top: 60px;
    border: 2px solid $second-color;
    border-radius: 25px;
    display: inline-block;
    padding: 8px 40px;
    margin-bottom: 50px;
    box-shadow: 0px 2px 6px 0px rgba(0, 0, 0, 0.3);
  }
}

.slides {
  background-color: $second-color;
  width: calc(100% - 350px);
  border-radius: 35px;
}
</style>