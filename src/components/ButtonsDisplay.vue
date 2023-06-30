<template>
    <div class="buttons-display">

        <!-- menu di navigazione -->
        <nav>
          <ul>
            <li>
                <a href=""><i class="fa-solid fa-house"></i></a>
            </li>
            <li>
                <a href=""><i class="fa-solid fa-user"></i></a>
            </li>
            <li>
                <a href=""><i class="fa-solid fa-graduation-cap"></i></a>
            </li>
            <li>
                <a href=""><i class="fa-solid fa-briefcase"></i></a>
            </li>
            <li>
                <a href=""><i class="fa-solid fa-book"></i></a>
            </li>
            <li>
                <a href=""><i class="fa-solid fa-address-card"></i></a>
            </li>
          </ul>
        </nav>

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

  ul {
    display: flex;
    flex-direction: column;
    align-items: center;

    li {
      margin-top: 13px;

      a {
        font-size: 25px;
        color: gray;
      }
    }
  }
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