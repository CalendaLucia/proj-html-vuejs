<script>
export default {
    name:'AppCourses',
    data() {
        return {


            data:[
                {
                    img: '/motivation-course-1.jpg',
                    cost: '$30',  decim: '.00',
                    description:'How to be Successful: Create A Growth Mindset For Success',
                    lessons: '3 Lessons' ,
                    users: '50 Studenst'
                },
                {
                    img: '/motivation-course-2.jpg',
                    cost: '$30',  decim: '.00',
                    description:'How to be Build Confidence in Your Abilities',
                    lessons: '1 Lessons' ,
                    users: '50 Studenst'
                },
                {
                    img: '/motivation-course-3.jpg',
                    cost: '$20',  decim: '.00',
                    description:'Profuctivity Machine - Focus in a Sistracted World',
                    lessons: '5 Lessons' ,
                    users: '50 Studenst'
                },
                {
                    img: '/motivation-course-4.jpg',
                    cost: '$20', decim: '.00',
                    description:'Effective Time Managemente Mastery - Complete Guide',
                    lessons: '18 Lessons' ,
                    users: '50 Studenst'
                },
                {
                    img: '/motivation-course-5.jpg',
                    cost: '$25', decim: '.99',
                    description:'Body Language Secrets for entrepreneurs',
                    lessons: '19 Lessons' ,
                    users: '50 Studenst'
                },
                {
                    img: '/motivation-course-6.jpg',
                    cost: '$19', decim: '.99',
                    description:'Management Skills: Thw Science of Leadership',
                    lessons: '17 Lessons' ,
                    users: '50 Studenst'
                }
            ] 
            
        }
    },

}
</script>

<template>
    <section id="courses">
        <div class="container">
            <div class="title">
                <p>BEGIN YOUR JOURNEY AT MAXCOACH</p>
                <h2 class="text">Latest <span>Online Courses</span></h2>
            </div>
            <div class="row">
                <div class="column"  v-for="item in data" :key="item.id">
                   <div class="card">
                      <img :src="`src/assets/images${item.img}`">
                   </div>
                   <div class="info-text">
                      <h5 class="cost"><span class="big"> {{ item.cost }}</span>{{ item.decim }}</h5>
                      <p class="description">{{ item.description }}</p>
                      <div class="icons">
                        <div class="lessons">
                            <font-awesome-icon class="myicon" icon="fa-regular fa-file-lines"/>
                            <span class="text">{{ item.lessons }}</span>
                        </div>
                        <div class="students">
                            <font-awesome-icon class="myicon" icon="fa-regular fa-user"/>
                            <span class="text">{{ item.users }}</span>
                        </div>
                      </div>
                   </div>
                </div>
            </div>
        </div>
        <div class="show-courses">
            <button type="text" class="start">
                 View all Courses 
                <font-awesome-icon icon="fa-solid fa-arrow-right-long" />
            </button>
        </div>
    </section>
</template>

<style lang="scss" scoped>

#courses {
    width: 100%;

    .container {
        width: 80%;
        margin: 0 auto;

        .title {
            text-align: center;
            padding-top: 100px;

            p {
                color: $link-color;
                font-size: 15px;
            }
            .text {
               font-size: 35px;
               font-weight: lighter;
               padding: 20px 0px;

            span {
                color: $secondary-color;
            }
        }

        }

        .row {
            padding-top: 30px;
            @include flex (space-between, center);
            flex-wrap: wrap;
            

            .column {
                width:calc((100% / 3) - 20px);
                margin: 30px 0px;
                transition: transform 0.3s;
                

                &:hover {
                    transform: translateY(-10px);
                    background-color: $background-color;
                }

                .card {
                    width: 100%;

                    img {
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                    }
                }
                .info-text {
                    padding: 10px 20px;

                    .cost {
                        color: $secondary-color;
                        font-size: 20px;
                        padding-bottom: 10px;

                        .big {
                           display: inline-block;
                           font-size: 25px;
                        }  
                    }
                    .description {
                        color: $hover-button-color;
                        font-size: 18px;
                        line-height: 1.4;
                        font-weight: bold;
                    }

                    .icons {
                        padding: 35px 0px;
                        @include flex (flex-start, center);

                        .students {
                           margin-left: 30px;
                        }

                          .myicon {
                            padding: 0px 5px;

                          }
                           
                       }
                       
                    }
                
            }
        }

    }

    .show-courses {
        width: 80%;
        margin: 0 auto;
        @include flex (center, center);

        .start {
            padding: 15px 55px;
            color: $primary-color;
            background-color: $secondary-color;
            font-weight: bold;
            border: none;
            border-radius: 5px;
           

            &:hover {
                background-color: $hover-button-color;
            }
        }
    }
   
}
</style>