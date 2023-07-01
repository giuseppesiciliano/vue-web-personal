<template>
    <div class="buttons-display">

        <!-- menu di navigazione -->
        <nav>
          <ul>
            <li>
                <span class="text" style="margin-right: -2px;">Home</span>
                <a><i id="home" class="fa-solid fa-house" @click="handleClick('home')"></i></a>
            </li>
            <li>
                <span class="text" style="margin-right: -4px;">Su di me</span>
                <a><i class="fa-solid fa-user" @click="handleClick('about-me')"></i></a>
            </li>
            <li>
                <span class="text">CV</span>
                <a><i class="fa-solid fa-graduation-cap" @click="handleClick('cv')"></i></a>
            </li>
            <li>
                <span class="text" style="margin-right: -3px;">Portfolio</span>
                <a><i class="fa-solid fa-briefcase"></i></a>
            </li>
            <li>
                <span class="text" style="margin-right: -4px;">Blog</span>
                <a><i class="fa-solid fa-book"></i></a>
            </li>
            <li>
                <span class="text" style="margin-right: -2px;">Contatti</span>
                <a><i class="fa-solid fa-address-card"></i></a>
            </li>
          </ul>
        </nav>

        <!-- avanti / indietro -->
        <div class="next-prev">
          <ul>
            <li>
              <span class="text" style="margin-right: -7px;">Avanti</span>
              <a><i class="fa-solid fa-chevron-right"></i></a>
            </li>

            <li>
              <span class="text" style="margin-right: -7px;">Indietro</span>
              <a><i class="fa-solid fa-chevron-left"></i></a>
            </li>
          </ul>
        </div>
    </div>
</template>


<script>
export default {
  name: 'ButtonsDisplay',
  methods: {
    handleClick(screen) {      
      this.$emit('button-click', screen);
    }
  }
}
</script>


<style scoped lang="scss">
@import '../style/variables';

nav, 
.next-prev {
  width: 70px;
  background-color: #6e0253;
  border-radius: 40px;
  box-shadow: 0px 0px 500px 0px rgba(0, 0, 0, 0.1);
}
nav ul,
.next-prev ul {
  display: flex;
  flex-direction: column;
  align-items: center;

  li {
    margin-top: 13px;
    position: relative;

    a {
      font-size: 25px;
      color: $second-color;
      transition: 0.2s ease-out;
          cursor: pointer;

      i {
        transition: 0.2s ease-out;
      }
    }
    a:hover {

      i {
        transform: scale(1.2);
      }
    }
  }
}

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
  height: 105px;
}

.text {
  visibility: hidden;
  opacity: 0;
  transition: 0.4s ease;
  position: absolute;
  right: 40px;
  cursor: pointer;
  color: $second-color;
  background-color: #01056b;
  white-space: nowrap;
  padding: 4px 8px;
}
.text:hover {
  display: none;
}

li:hover {
  .text {
    visibility: visible;
    opacity: 1;
    transform: translateX(-10px);
  }
}
</style>