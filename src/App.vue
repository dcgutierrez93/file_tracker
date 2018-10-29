<template>
  <div id="app">
    <AppHeader></AppHeader>
    <AppSideNav></AppSideNav>
    <Main></Main>

  </div>
</template>

<script>
import Main from './components/Main.vue'
import Header from './components/Header.vue'
import SideNav from './components/SideNav.vue'

export default {
  name: 'app',
  components: {
      AppHeader: Header,
      AppSideNav: SideNav,
      Main: Main
  }
}
</script>
