<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
export default {
  name:'App',
  data() {
    return {
      menuItems: [
        
           {label: 'Home', url: '#', arrow:'fa-solid fa-angle-down',},
           {label: 'Pages', url: '#', arrow:'fa-solid fa-angle-down'},
           {label: 'Courses', url: '#', arrow:'fa-solid fa-angle-down'},
           {label: 'Features', url: '#', arrow:'fa-solid fa-angle-down'},
           {label: 'Blog', url: '#', arrow:'fa-solid fa-angle-down'},
           {label: 'Shop', url: '#', arrow:'fa-solid fa-angle-down'},
      ],
      icons: [
           {icon: 'fa-brands fa-twitter'},
           {icon: 'fa-brands fa-facebook-f'},
           {icon: 'fa-brands fa-instagram'},
           {icon: 'fa-brands fa-linkedin'}
      ],
      dropdown:[
                 {label: 'Start Here', url: '#'},
                 {label: 'Success Story', url: '#'},
                 {label: 'About me', url: '#'},
                 {label: 'About me 01', url: '#'},
                 {label: 'About me 02', url: '#'},
                 {label: 'About me 03', url: '#'},
                 {label: 'Contact me', url: '#'},
                 {label: 'Contact us', url: '#'},
                 {label: 'Purchase Guide', url: '#'},
                 {label: 'Privacy Policy', url: '#'},
                 {label: 'Terms of Service', url: '#'},
               ]     
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
 <AppFooter/>
</template>

<style lang="scss">
#app {
  width: 100%;
}
</style>
