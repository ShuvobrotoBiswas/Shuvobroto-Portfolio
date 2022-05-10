<template>
  <div class="q-pa-md">
    <q-carousel
      animated
      v-model="slide"
      infinite
      :autoplay="autoplay"
      transition-prev="slide-right"
      transition-next="slide-left"
      @mouseenter="autoplay = false"
      @mouseleave="autoplay = true"
    >
      <q-carousel-slide name="first" img-src="~assets/img1.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h4">Hello! This is Shuvobroto Biswas</div>
          <div class="text-subtitle1">
            Frontend Developer | Cross Platform Software
          </div>
          <!-- My CV -->
          <transition
            appear
            enter-active-class="animated fadeIn"
            leave-active-class="animated fadeOut"
          >
            <q-btn
              color="black"
              icon="collections_bookmark"
              label="My CV"
              href="https://drive.google.com/file/d/1I-fWsqrag8q2FUqDbuh5qwAsz9yrUKoO/view?usp=sharing"
            />
          </transition>
          <!-- My Professional Achievements -->
          <transition
            appear
            enter-active-class="animated fadeIn"
            leave-active-class="animated fadeOut"
          >
            <q-btn
              color="black"
              icon="workspace_premium"
              label="My Professional Achievements"
              href="https://drive.google.com/file/d/1RQ4vjFD4AfDU9_siWRQA-rLu9UkNmhsI/view?usp=sharing"
            />
          </transition>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="second" img-src="~assets/img2.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h3">Vue JS</div>
          <div class="text-subtitle1">I working with this framework</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="third" img-src="~assets/img3.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h3">Quasar JS</div>
          <div class="text-subtitle1">I working with this framework</div>
        </div>
      </q-carousel-slide>
    </q-carousel>
  </div>
  <div class="text-h4 row justify-center items-center">About Me</div>

  <!-- Break -->

  <!-- <div class="flex-break q-py-md"></div> -->
  <div class="q-pa-md row justify-center items-center">
    Frontend Developer (Software) | Vue.js | Quasar js | Figma | Javascript |
    Git | Node.js . I completed an Internship on Vue js & Quasar at IT Conquest
    , Canada ( https://www.itconquest.com/ ). There was spent great time ever ,
    I was learned many programming to be a software developer like , Node js ,
    SASS , SCSS , Javascript , Vue , Quasar , VueX , Rest APIs , Git, Time
    managements , Company behavior , Responsibility and many more . Now I'm
    responsible software engineer.
  </div>

  <!-- My Experiences -->
  <div class="text-h4 row justify-center items-center">My Experiences</div>

  <!-- Break -->

  <div class="flex-break q-py-md"></div>

  <!-- My Experiences -->

  <div class="text-h5 row justify-center items-center">
    <div class="flex flex-center">
      <q-btn href="https://vuejs.org/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img4.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://quasar.dev/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img5.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://www.w3schools.com/js/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img6.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://www.google.com/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img7.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://nodejs.org/en/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img8.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn
        href="https://www.figma.com/file/bLB9CgK4FHDfKZXCpx0bl2/GPS-Tracking-APP?node-id=0%3A1"
      >
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img9.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://github.com/ShuvobrotoBiswas">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img10.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
      <q-btn href="https://reactjs.org/">
        <img
          class="q-pa-xs"
          alt="Laptop logo"
          src="~assets/img11.png"
          style="width: 50px; height: 50px"
        />
      </q-btn>
    </div>
  </div>

  <!-- About Me Popup -->

  <div class="q-pa-md q-gutter-sm fixed-bottom-right">
    <q-btn
      icon="favorite"
      round
      class="q-ma-md"
      color="black"
      @click="alert = true"
    />
    <q-dialog v-model="alert">
      <q-card>
        <q-card-section>
          <div class="text-h6">About me</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          Frontend Developer (Software) | Vue.js | Quasar js | Figma |
          Javascript | Git | Node.js | Internship Completed at IT Conquest,
          Canada
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      slide: ref("first"),
      autoplay: ref(true),
      alert: ref(false),
      prompt: false,
      submit: " ",
      cancel: "",
    };
  },
};
</script>

<style lang="sass" scoped>
.custom-caption
  text-align: center
  padding: 12px
  color: white
  background-color: rgba(0, 0, 0, .3) ,

.my-emoji
  vertical-align: middle
  height: 2em
  width: 2em
</style>
