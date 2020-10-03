<template>
  <div>
    <the-header @sidenavToggle = "displaySidenav = !displaySidenav"></the-header>
    <the-side-nav
    :show="displaySidenav"
    @close="displaySidenav = false">
    </the-side-nav>
    <Nuxt />
  </div>
</template>

<script>
import TheHeader from '@/components/Navigation/TheHeader.vue'
import TheSideNav from '@/components/Navigation/TheSideNav.vue'
export default {
  components: {
    TheHeader,
    TheSideNav,
  },
  data() {
    return {
      displaySidenav: false,
    }
  },
}
</script>
<style>
html {
  font-family: 'Open Sans', sans-serif;
}

body {
  margin: 0;
}
</style>
