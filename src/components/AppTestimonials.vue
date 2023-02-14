<script>
export default {
    name:'AppTestimonal',
    data() {
        return {
            
        }
    },
}
</script>

<template>
   <section id="testimonials">
      <div class="container">
        <div class="row">
            <div class="column">
                <div class="feedback">
                   <p class="text-color">REAL STORIES</p>
                   <p>I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.</p>
                </div>
                <div class="image">
                    <img src="../assets/images/testimonial-avata-02.jpg">
                </div>
                <div class="name-user">
                    <p class="name">Mina Hollace</p>
                    <p>/ Freelancer</p>
                </div>
            </div>
            <div class="column">
               <div class="model">
                  <img src="../assets/images/home-movation-testimonial-image-768x562.jpg">
               </div>
            </div>
            <div class="counter-image">
                <img class="up" src="../assets/images/arrow-up.png">
                <p>1/4</p>
                <img class="down" src="../assets/images/arrow-down.png">
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
                    width: 45%;
                    
                    .text-color {
                        color: $secondary-color;
                        margin-top: 40px;
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
                    

                    img {
                        width: 100%;
                        height: 100%;
                        border-radius: 50%;
                        object-fit: cover;
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
                         margin-top: 5px;
                    }

                    .down {
                        padding-top: 25px;
                    }
                }

        }
    }
}
</style>