<script>
export default {
    name:'AppBlog',
    data() {
        return {

            data: [
                {
                    time:'May 13, 2020', 
                    info:'How to Stay true to Your Personal Brand',
                    text:"When it comes to your business or career, you want..."
                },
                {
                    time:'May 13, 2020', 
                    info:'5 Vital Lessons in 5 Years of Freelancing',
                    text:"Being self-employed and workin from home, it's easy to get..."
                },
                {
                    time:'May 13, 2020', 
                    info:'11 Super Useful Tips for Small-Business Owners',
                    text:"Being a small business owner poses a ton of challenges. We ..."
                },
                {
                    time:'May 13, 2020', 
                    info:'How to Give Yourself Grace to Start Again',
                    text:"Forgive yourself for bad habits you may have started or ..."
                },
            ]
            
        }
    },
}
</script>

<template>
    <section id="blog">
        <div class="container">
            <div class="row">
                <div class="column large">
                    <p class="title">BLOG UPDATED</p>
                    <p class="description">
                        Interesting 
                        <span class="text-color">
                            articles updated 
                        </span> 
                        daily
                    </p>
                </div>
                <div class="row flex">
                    <div class="column " v-for="item in data" :key="item.id">
                        <div class="card">
                            <img src="../assets/images/motivation-blog-04-480x325.jpg">
                        </div>
                        <div class="text-info">
                            <font-awesome-icon class="myicon" icon="fa-regular fa-calendar"/>
                            <p class="time"> {{ item.time }}</p>
                            <p class="info"> {{ item.info }}</p>
                            <p class="text"> {{ item.text }}</p>
                        </div> 
                    </div>
                </div>
            </div>
            <div class="all-post">
                <a href="#" class="text-color">
                    VIEW ALL POSTS
                </a>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

#blog {
    width: 100%;
    padding-top: 80px;

    .container {
        width: 80%;
        margin: 0 auto;

        .row {

            .flex {
                @include flex (center, center);
            }
            .column {
                width: calc(100% / 4);
                margin: 0px 15px;

                 .title {
                       font-size: 15px;
                       color: $link-color;
                       padding: 20px 0px;
                 }

                 .description {
                     font-size: 30px;
                     padding-bottom: 50px;

                    .text-color {
                        color: $secondary-color;
                    }
                 }

                 .card {
                  width: 100%;
                  height: 100%;
                
                    img {
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                    }
  
                 }

                 .text-info {
                      padding: 20px 0px;
                      line-height: 1.5;
                    
                      .time {
                         display: inline-block;
                         margin-left: 10px;
                      }
                        .info {
                           padding: 5px 0px;
                           font-size: 15px;
                           font-weight: bold;
                        }

                        .text {
                            color: $link-color;
                            padding: 10px 0px;
                        }
                        
                 }
              }
            .large {
                    width: 100%;
                }
        }

        .all-post {
            width: 50%;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            padding: 20px 0px;
            .text-color {
                color: $secondary-color;
                
            }
        

        }
    }
}
</style>