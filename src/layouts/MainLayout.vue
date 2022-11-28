<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-black">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />
        <q-toolbar-title> SHUVOBROTO PORTFOLIO </q-toolbar-title>
        <!-- <div>Quasar v{{ $q.version }}</div> -->
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <div>
        <q-img
          class="absolute-top"
          src="~assets/cover.png"
          style="height: 200px"
        >
          <div class="absolute-bottom bg-transparent">
            <q-avatar size="100px" class="q-mb-sm">
              <img src="~assets/profile.png" />
            </q-avatar>
            <div class="text-weight-bold">Shuvobroto Biswas</div>
            <div>Software Engineer</div>
          </div>
        </q-img>
      </div>
      <div>
        <q-scroll-area
          style="
            height: calc(100% - 150px);
            margin-top: 200px;
            border-right: 1px solid #ddd;
          "
        ></q-scroll-area>
        <q-list>
          <q-item-label header>My Essential Links </q-item-label>

          <EssentialLink
            v-for="link in essentialLinks"
            :key="link.title"
            v-bind="link"
          />
        </q-list>
      </div>
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>

    <!-- Footer -->
    <q-footer class="bg-black absolute-bottom">
      <div class="row justify-center items-center">
        2022 © Shuvobroto™ All rights reserved.
      </div>
    </q-footer>
  </q-layout>
</template>
<script>
import EssentialLink from "components/EssentialLink.vue";

const linksList = [
  {
    title: "Educations & CV",
    caption: "Green University of Bangladesh --    BSC in CSE (2018-2022)",
    icon: "school",
    link: "https://drive.google.com/file/d/1I-fWsqrag8q2FUqDbuh5qwAsz9yrUKoO/view?usp=sharing",
  },
  {
    title: "Github",
    caption: "github.com/ShuvobrotoBiswas",
    icon: "code",
    link: "https://github.com/ShuvobrotoBiswas",
  },
  // {
  //   title: "Discord Chat Channel",
  //   caption: "chat.quasar.dev",
  //   icon: "chat",
  //   link: "https://chat.quasar.dev",
  // },
  {
    title: "Facebook",
    caption: "facebook/Shuvobroto(Rocky)",
    icon: "facebook",
    link: "https://www.facebook.com/Coder.Rocky.Samrat.Devils.King.Software.Developer/",
  },
  {
    title: "Twitter",
    caption: "twitter.com/ShuvobrotoB",
    icon: "person",
    link: "https://twitter.com/ShuvobrotoB",
  },
  {
    title: "Linkedin",
    caption: "Linkedin/Shuvobroto",
    icon: "task_alt",
    link: "https://www.linkedin.com/in/shuvobroto-biswas-58a045193/",
  },
  // {
  //   title: "Quasar Awesome",
  //   caption: "Community Quasar projects",
  //   icon: "favorite",
  //   link: "https://awesome.quasar.dev",
  // },
];

import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    EssentialLink,
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
