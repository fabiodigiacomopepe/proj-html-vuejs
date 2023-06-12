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
  <PageFooter />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;
@use './styles/partials/mixins.scss' as *;
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
</style>
