<template>
    <div class="main-display">

      <!-- profilo -->
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

      <!-- screens -->
      <Home v-if="showHome" />
      <AboutMe v-if="showAboutMe" :class="{ flip: clicked }" />
      <CV v-if="showCV" :class="{ rotate: clicked }" />
      <Portfolio v-if="showPortfolio" />
      <Blog v-if="showBlog" />
      <Contact v-if="showContact" />

    </div>
</template>


<script>
import Home from './Home.vue';
import AboutMe from './AboutMe.vue';
import CV from './CV.vue';
import Portfolio from './Portfolio.vue';
import Blog from './Blog.vue';
import Contact from './Contact.vue';


export default {
  name: 'MainDisplay',
  components: {
    Home,
    AboutMe,
    CV,
    Portfolio,
    Blog,
    Contact
  },
  data() {
    return {
      showHome: true,
      showAboutMe: false,
      showCV: false,
      showPortfolio: false,
      showBlog: false,
      showContact: false,

      clicked: true,
    }
  },
  methods: {
    showScreen(screen) {

      const screens = {
        'home': 'showHome',
        'about-me': 'showAboutMe',
        'cv': 'showCV',
        'portfolio': 'showPortfolio',
        'blog': 'showBlog',
        'contact': 'showContact'
      };

      Object.keys(screens).forEach((prop) => {
        this[screens[prop]] = (prop === screen);
      });
    }
  }
}
</script>


<style scoped lang="scss">
@import '../style/variables';
@import '../style/generals';

.main-display {
  background-color: #6e0253;
  border-radius: 35px;
  box-shadow: 0px 20px 500px 10px rgba(0, 0, 0, 0.3);
  width: calc(100% - 100px);
  overflow: hidden;
  display: flex;
}

.profilo {
  background: linear-gradient(90deg, rgba(1,5,107,1) 0%, rgba(110,2,83,1) 76%);
  min-width: 350px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;

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



// effetti al cambio di screen
.flip {
  animation: flip-horizontal-bottom 1s cubic-bezier(0.455, 0.030, 0.515, 0.955) both;
}
@keyframes flip-horizontal-bottom {
  0% {
    transform: rotateX(0);
  }
  50% {
    transform: rotateX(90deg);
  }
  100% {
    transform: rotateX(0deg);
  }
}

.rotate {
  animation: rotate-center 0.6s ease-in-out both;
}

@keyframes rotate-center {
  0% {
    transform: rotate(0);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>