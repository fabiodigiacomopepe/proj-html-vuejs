<script>
import { store } from './store.js'

import PageHeader from './components/PageHeader.vue'
import AppNavBar from './components/AppNavBar.vue'
import AppJumbotron from './components/AppJumbotron.vue'
import AppPartner from "./components/AppPartner.vue"

import PageMain from './components/PageMain.vue'
import AppKeyFeatures from './components/AppKeyFeatures.vue';
import AppQuickStart from './components/AppQuickStart.vue';
import AppBuildTools from './components/AppBuildTools.vue';
import AppPrice from './components/AppPrice.vue';
import AppGetStarted from './components/AppGetStarted.vue';

import PageFooter from './components/PageFooter.vue'

export default {
  components: {
    PageHeader,
    AppNavBar,
    AppJumbotron,
    AppPartner,
    PageMain,
    AppKeyFeatures,
    AppQuickStart,
    AppBuildTools,
    AppPrice,
    AppGetStarted,
    PageFooter,
  },
  data() {
    return {
      store,
      menuHeader: [
        {
          name: "home",
          url: "#",
          dropdown: false
        },
        {
          name: "landing",
          url: "#",
          dropdown: true
        },
        {
          name: "pages",
          url: "#",
          dropdown: true
        },
        {
          name: "docs",
          url: "#",
          dropdown: true
        },
      ],
      company: [
        {
          name: "About us",
          url: "#",
          active: false,
        },
        {
          name: "Services",
          url: "#",
          active: false,
        },
        {
          name: "Team",
          url: "#",
          active: false,
        },
        {
          name: "Pricing",
          url: "#",
          active: false,
        },
        {
          name: "Project",
          url: "#",
          active: false,
        },
        {
          name: "Careers",
          url: "#",
          active: false,
        },
        {
          name: "Blog",
          url: "#",
          active: false,
        },
        {
          name: "Login",
          url: "#",
          active: false,
        },
      ],
      usefullLinks: [
        {
          name: "Terms of Services",
          url: "#",
          active: false,
        },
        {
          name: "Privacy Policy",
          url: "#",
          active: false,
        },
        {
          name: "Documentation",
          url: "#",
          active: false,
        },
        {
          name: "Changelog",
          url: "#",
          active: false,
        },
        {
          name: "Components",
          url: "#",
          active: false,
        }
      ]
    }
  },
  methods: {

  },
  created() {

  }
}
</script>

<template>
  <header>
    <PageHeader :vociMenuHeader="menuHeader" />
  </header>

  <main>
    <PageMain />
  </main>

  <PageFooter :vociCompany="company" :vociUsefullLinks="usefullLinks" />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;
@use './styles/partials/mixins.scss' as *;
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
</style>
