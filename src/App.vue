<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import menuItems from './data.json'
export default {
  name:'App',
  data() {
    return {
      menuItems: menuItems.menuItems,
      icons: menuItems.icons,
      dropdown: menuItems.dropdown,
      address: menuItems.address,
      social: menuItems.social,
      explore:menuItems.explore,
      information: menuItems.information
    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>
 <AppHeader :menuItems="menuItems" :icons="icons" :dropdown="dropdown"/>
 <AppMain :statsNumber="statsNumber"/>
 <AppFooter :address="address" :social="social" :explore="explore" :information="information"/>
</template>

<style lang="scss">
#app {
  width: 100%;
}
</style>
