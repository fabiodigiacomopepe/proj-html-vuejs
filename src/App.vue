<script>
import { store } from './store.js'
import PageHeader from './components/PageHeader.vue'
import PageMain from './components/PageMain.vue'
import PageFooter from './components/PageFooter.vue'

export default {
  components: {
    PageHeader,
    PageMain,
    PageFooter,
  },
  data() {
    return {
      store,
      menuHeader: [
        {
          name: "home",
          url: "#",
          active: false,
          dropdown: false
        },
        {
          name: "landing",
          url: "#",
          active: true,
          dropdown: true
        },
        {
          name: "pages",
          url: "#",
          active: false,
          dropdown: true
        },
        {
          name: "docs",
          url: "#",
          active: false,
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
  <PageHeader :vociMenuHeader="menuHeader" />
  <PageMain />
  <PageFooter :vociCompany="company" :vociUsefullLinks="usefullLinks" />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;
@use './styles/partials/mixins.scss' as *;
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
</style>
