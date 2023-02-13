<script>
export default {
    name:'AppHeader',
     data() {
        return {
            
        }
     },
     props: {
        menuItems: {
            type: Array,
            required: true,
        },
        logo: {
           type: String,
           required: true,
        },

     }
    
}

</script>

<template>
  <header>
    <section class="nav-bar">
        <nav>
            <div class="logo">
                <img src="../assets/images/dark-logo.png" alt="logo">
            </div>
            <div class="group-list">
                <ul>
                    <li v-for="item in menuItems" :key="item.label">
                        <a :href="item.url">
                            {{ item.label }}
                        </a>
                    </li>
                </ul>
            </div>
            <div class="group-icons">
                <ul>
                    <li></li>
                </ul>
            </div>
        </nav>
    </section>
  </header>
</template>

<style lang="scss" scoped>

</style>
