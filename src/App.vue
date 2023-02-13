<script>
import AppHeader from './components/AppHeader.vue'
export default {
  name:'App',
  data() {
    return {
      menuItems: [
           {label: 'Home', url: '#'},
           {label: 'Pages', url: '#'},
           {label: 'Courses', url: '#'},
           {label: 'Features', url: '#'},
           {label: 'Blog', url: '#'},
           {label: 'Shop', url: '#'},
      ],
      icons: [
           {icon: 'fa-brands fa-linkedin'},
           {icon: 'fa-brands fa-facebook'},
           {icon: 'fa-brands fa-instagram'},
           {icon: 'fa-brands fa-linkedin'},
      ]     
    }
  },
  components: {
    AppHeader
  }
}
</script>

<template>
 <AppHeader :menu-items="menuItems" :icons="icons"/>
</template>

<style lang="scss">
</style>
