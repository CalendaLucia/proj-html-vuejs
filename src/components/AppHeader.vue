<script>
import AppDropDown from './AppDropDown.vue'
import AppJumbotron from './AppJumbotron.vue'
export default {
    name:'AppHeader',
     data() {
        return {
          active: false,
          activeIndex: -1,
          activeDropdownIndex: -1

        }
     },
     components: {
         AppDropDown,
         AppJumbotron
     },
     props: {
       menuItems: {
            type: Array,
            required: true,
       },

       dropdown: {
            type: Array,
            required: true,
       },

       icons: {
            type: Array,
            required: true,
       },

     },
     methods: {
      toggle(index) {
         if (this.activeIndex === index) {
             this.activeIndex = -1; // chiude il dropdown se la stessa icona è cliccata di nuovo
         } else {
             this.activeIndex = index; // apre il dropdown corrispondente
            }
      },
      
   }
         
 }
  
</script>

<template>
  <header>
    <section id="nav-bar">
        <nav>
            <div class="logo">
                <img src="../assets/images/dark-logo.png" alt="logo">
            </div>
            <div class="group-list">
                <ul class="list-item-menu">
                    <li class="item-menu"  v-for="(item, index) in menuItems" :key="item.label" @click="toggle(index)">
                        <a class="link-menu" :href="item.url">
                            {{ item.label }} 
                            <font-awesome-icon :icon="item.arrow" class="icon"/>
                        </a>
                        <AppDropDown class="AppDropDown" v-if="activeIndex === index" :dropdown="dropdown"/>
                    </li>
                </ul>
            </div>
            <div class="group-icons">
                <ul class="list-icon-menu">
                    <li class="item-icons" v-for="icon in icons" :key="icon.icon">
                        <a class="link-icon" href="#">
                           <font-awesome-icon :icon="icon.icon" class="arrow"/>
                        </a>
                    </li>
                </ul>
            </div>
        </nav>
    </section>
    <AppJumbotron/>
  </header>
</template>

<style lang="scss" scoped>

header {
  width: 100%;
  max-width: 100%;
  padding: 10px 0px;
  background-color: $background-color;
  background-image: url(../assets/images/background-pattern-wavify.png);
 
  #nav-bar {
    width: 80%;
    margin: 0 auto;

    nav {
      @include flex (space-around, center);

      .logo {
        width: 20%;

        img {
          width: 100px;
        }
      }

      & .group-list, 
         
      & .group-icons {

        ul {
          list-style: none;

          li {
            display: inline;
            
            a {
              text-decoration: none;
              font-size: 15px;
    
              .icon {
                font-size: 10px;
              }
            }
          }
        }
      }

      & .group-list {
        width: 60%;
       
        & .list-item-menu {
             @include flex (center, center);
             position: relative;

             .AppDropDown {
               position: absolute;
               top: 0px; 
               z-index: 1000;
               background-color: $background-color;
              }
        }
        & .item-menu {
            padding: 0px 20px;

            .link-menu {
                color: $link-color;
                

                &:hover {
                    color:$secondary-color;
                    border-bottom: 1px solid $secondary-color;
                    
                }
            }
        }
      }

      & .group-icons {
            width: 20%;
            margin-left: 30px;

        & .item-icons {
            padding: 0px 10px;

            .link-icon {
                color: black;
            }
            
        }

        .arrow {
            font-size: 15px;
        }
      }
    }
  }
}

</style>
