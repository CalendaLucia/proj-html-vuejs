<script>
export default {
    name:'AppTestimonal',
    data() {
        return {
            current: 0,

            images: [
            {
                  src: '/testimonial-avata-02.jpg',
                  text: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus.Great study for people like me.',
                  name: 'Mina Hollance',
                  title: '/Freelancer'
               },

              {
                  src: '/testimonial-avata-01.jpg',
                  text: 'I always had a passion for learning web development but never had the time or resources to do so. DevCamp has given me the flexibility and support to pursue my dream while still working a full-time job.',
                  name: 'John Doe',
                  title: 'Web Developer'
               },
               {
                  src: '/testimonial-avata-03.jpg',
                  text: 'The instructors are top notch. They make the material interesting and easy to understand. I have improved a lot since starting the DevCamp program.',
                  name: 'Jane Smith',
                  title: 'Designer'
               },
               {
                  src: '/testimonial-avata-04.jpg',
                  text: 'DevCamp has helped me develop the skills needed to transition from my previous career as a graphic designer to a full-time front-end developer. I am grateful for the opportunity.',
                  name: 'Bob Johnson',
                  title: 'Front-end Developer'
               },            
]
        }
    },
    methods: {
       nextImage() {
          this.current++;

          if (this.current >= this.images.length - 1) {
              this.current = 0;
           }

          
        },

        prevImage() {
            this.current--;

             if (this.current < 0) {
                 this.current = this.images - 1;
              }

             this.current = this.current;
         }
}

}
</script>

<template>
  <section id="testimonials">
    <div class="container">
      <div class="row">
        <div class="column">
          <div class="feedback">
            <p class="text-color">REAL STORIES</p>
            <p>{{ images[current].text }}</p>
          </div>
          <div class="image">
            <div class="slider">
                <div class="slides" >
                    <div class="slide" v-for="(image, index) in images" :key="index">
                        <img  v-if="current == index" :src="`src/assets/images${images[current].src}`" />
                    </div>
                </div>
            </div>
          </div>
          <div class="name-user">
            <p class="name">{{ images[current].name }}</p>
            <p>/ {{ images[current].title }}</p>
          </div>
        </div>
        <div class="column">
          <div class="model">
            <img src='../assets/images/home-movation-testimonial-image.jpg' />
          </div>
        </div>
        <div class="counter-image">
          <img class="up" src="../assets/images/arrow-up.png" @click="nextImage" />
          <p>{{ current + 1 }}/{{ images.length }}</p>
          <img class="down" src="../assets/images/arrow-down.png" @click="prevImage" />
        </div>
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>

#testimonials {
    width: 100%;
    padding-top: 30px;
 
    .container {
        width: 100%;
        position: relative;

        .row {
            width: 100%;
            @include flex (center,center);
          
            
            .column {
                width: calc(100% / 2);
                height: 400px;
                @include flex (center,center);
                flex-direction: column;
                background-image: url(../assets/images/background-pattern-wavify.png);
                background-repeat: no-repeat;
                background-color: $background-color;

                .feedback {
                    text-align: center;
                     width: 80%;
                     font-size: 20px;
                    
                    .text-color {
                        color: $secondary-color;
                        margin-top: 40px;
                        font-size: 12px;
                        font-weight: bold;
                    }
                    p {
                        line-height: 1.8;
                        padding-bottom: 30px;
                    }
                }
                
                .image {
                    width: 60px;
                    height: 60px;
                    border-radius: 50%;

                    .slider {
                        width: 100%;
                        height: 100%;
                        .slides {
                             width: 100%;
                             height: 100%;

                              
                                img {
                                 width: 100%;
                                 height: 100%;
                                 border-radius: 50%;
                                 object-fit: cover;
                             }
                            

                        }
                    }
                    

                 
                }

                .name-user {
                    padding: 10px 0px;

                    .name {
                        padding: 8px;
                        font-size: 15px;
                    }

                    p {
                        font-size: 10px;
                        text-align: center;
                        padding-top: 5px;
                    }
                }

                .model {
                    width: 100%;
                    height: 100%;
                   

                    img {
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                        
                    }
                }

            }

            .counter-image {
                    background-color: $primary-color;
                    position: absolute;
                    top: 50%;
                    left: 50%;
                    transform: translate( -50%, -50%);
                    z-index: 9999;
                    width: 75px;
                    height: 75px;
                    border-radius: 50%;
                    padding: 10px 0px;

                    img {
                        margin-left: 50%;
                        transform: translate( -50%, -50%);
                    }

                    p {
                        text-align: center;
    
                    }

                    .down {
                        padding-top: 20px;
                    }
                }

        }
    }
}
</style>