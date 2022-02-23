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
          <div class="text-subtitle1">Frontend Developer | Cross Platform Software</div>
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
  <div class="text-h4 row justify-center items-center">
    My Experiences
  </div>

  <div class="flex-break q-py-md"></div>

 <div class="text-h5 row justify-center items-center">
  <div class="flex flex-center">
    <q-btn href="https://vuejs.org/">
     <img class="q-pa-xs"
      alt="Laptop logo"
      src="~assets/img4.png"
      style="width: 50px; height: 50px"
    />
    </q-btn>
    <q-btn href="https://quasar.dev/">
     <img class="q-pa-xs"
      alt="Laptop logo"
      src="~assets/img5.png"
      style="width: 50px; height: 50px"
    />
    </q-btn>
    <q-btn href="https://www.w3schools.com/js/">
     <img class="q-pa-xs"
      alt="Laptop logo"
      src="~assets/img6.png"
      style="width: 50px; height: 50px"
    />
    </q-btn>
    <q-btn href="https://www.google.com/">
     <img class="q-pa-xs"
      alt="Laptop logo"
      src="~assets/img7.png"
      style="width: 50px; height: 50px"
    />
    </q-btn>
    <q-btn href="https://nodejs.org/en/">
     <img class="q-pa-xs"
      alt="Laptop logo"
      src="~assets/img8.png"
      style="width: 50px; height: 50px"
    />
    </q-btn>
    <q-btn href="https://www.figma.com/file/bLB9CgK4FHDfKZXCpx0bl2/GPS-Tracking-APP?node-id=0%3A1">
     <img class="q-pa-xs"
      alt="Laptop logo"
      src="~assets/img9.png"
      style="width: 50px; height: 50px"
    />
    </q-btn>
    <q-btn href="https://github.com/ShuvobrotoBiswas">
     <img class="q-pa-xs"
      alt="Laptop logo"
      src="~assets/img10.png"
      style="width: 50px; height: 50px"
    />
    </q-btn>
    <q-btn href="https://reactjs.org/">
     <img class="q-pa-xs"
      alt="Laptop logo"
      src="~assets/img11.png"
      style="width: 50px; height: 50px"
    />
    </q-btn>
   </div>
  </div>

  <div class="q-pa-md q-gutter-sm fixed-bottom-right " >
    <q-btn
      @click="prompt = true"
      id="add"
      round
      color="primary"
      icon="chat"
      class="q-ma-md bg-black "
    />
    </div>
    <!-- <q-dialog v-model="prompt" persistent>
      <q-card style="min-width: 350px">
        <q-card-section>
        <div class="q-pa-md row justify-center">
    <div style="width: 100%; max-width: 350x">
      <q-chat-message
        :text="['Have you seen Quasar?']"
        sent
        text-color="white"
        bg-color="primary"
      >
        <template v-slot:name>me</template>
        <template v-slot:stamp>7 minutes ago</template>
        <template v-slot:avatar>
          <img
            class="q-message-avatar q-message-avatar--sent"
            src="https://cdn.quasar.dev/img/avatar4.jpg"
          >
        </template>
      </q-chat-message>

      <q-chat-message
        bg-color="amber"
      >
        <template v-slot:name>Mary</template>
        <template v-slot:avatar>
          <img
            class="q-message-avatar q-message-avatar--received"
            src="https://cdn.quasar.dev/img/avatar2.jpg"
          >
        </template>

        <div>
          Already building an app with it...
          <img src="https://cdn.quasar.dev/img/discord-qeart.png" class="my-emoji">
        </div>

        <q-spinner-dots size="2rem" />
        </q-chat-message>
       </div>
       </div>
       <div>
        <q-btn class="q-mt-xl" color="gray" text-color="#ddd"
                unelevated
                label="Cancel"
                no-caps
                v-close-popup
              />
         <q-btn
                class="q-mt-xl"
                color="blue"
                text-color="white"
                unelevated
                label="Save"
                type="submit"
                no-caps
                v-close-popup
              />
      </div>
        </q-card-section>
      </q-card>
    </q-dialog> -->


</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      slide: ref('first'),
      autoplay: ref(true),
      prompt: false,
      submit: " ",
      cancel: "",
    }
  }
}
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
