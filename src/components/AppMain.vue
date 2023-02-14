<script>
import AppAboutMe from './AppAboutMe.vue'
import AppCourses from './AppCourses.vue'
import AppBookStore from './AppBookStore.vue'
import AppTestimonials from './AppTestimonials.vue'
import AppBlog from './AppBlog.vue'
export default {
    name: 'AppMain',
    data() {
        return {
            

            statsNumber : [
                {id:1, number:'1.926', text:'FINISCHED SESSIONS'},
                {id:2, number:'100%', text:'SATISFACTION RATE'},
                {id:3, number:'3092+', text:'ENROLLED LEARNERS'},
                {id:4, number:'200', text:'ONLINE INSTRUCTIONS'},
            ]
            
        }
    },
    components: {
        AppAboutMe,
        AppCourses,
        AppBookStore,
        AppTestimonials,
        AppBlog
    },
  
}
</script>

<template>
   <main>
      <section id="stats">
         <div class="container">
            <div class="column" v-for="item in statsNumber" :key="item.id">
                <p class="number"> {{ item.number }}</p>
                <p class="text-label">{{ item.text }}</p>
                <div class="grid-line">
                    <img src="../assets/images/background-pattern-grid-line-06.png">
                </div>
            </div>
         </div>
      </section>
      <AppAboutMe/>
      <AppCourses />
      <AppBookStore/>
      <AppTestimonials/>
      <AppBlog/>
   </main>
</template>

<style lang="scss" scoped>
#stats {
    padding: 50px 0px;
    width: 100%;
    max-width: 100%;

    .container {
        width: 80%;
        margin: 0 auto;
        @include flex (space-between, center);

        .column {
            width: calc(100% / 4);
            margin: 0px 10px;
            text-align: center;
            position: relative;
            padding: 10px 0px;

            .number {
                color: $secondary-color;
                font-size: 20px;
               
            }

            .text-label {
                padding: 10px 0px;
                font-size: 10px;
            }

            .grid-line {
              width:100% ;
              position: absolute;
              top: 0px;
              left: 10px;

              img {
                width: 100%;
                object-fit: cover ;
              }
            }
            
        }
    }
}
</style>