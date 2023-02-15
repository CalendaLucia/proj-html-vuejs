<script>
export default {
    name:'AppAboutMe',
    data() {
        return {
            
        }
    },
}
</script>

<template>
   <section id="about-me">
      <div class="container">
        <div class="row">
           <div class="column how-to-be">
              <h3>ABOUT ME</h3>
              <p>How to Be an Alpha Male: The 15 Habits of True Alphas</p>
            </div>
            <div class="column want-to-learn">
               <p class="introduction-text"> Want to learn how to be <span class="text-color"> an alpha male </span> ? How to be more masculine? How to be the man 
                   you've always wanted to be?
               </p>
               <p class="other-text">
                  Your goal is to show the consistency of business, core values, and customer care.
                   Punctuality, responsability, individuality, accuracy, enthusiasm - you have to clearly
                   explain how these qualities are applicable to you work. And the important thingh is you 
                   do love whath you do.
                </p>
            </div>
        </div> 
        <div class="row">
           <div class="column video">
              <img class="img-video" src="../assets/images/home-movation-video-poster-670x450.jpg">
              <img class="youtube" src="../assets/images/icon-youtube-play.png">
           </div>
           <div class="column cit">
               <p class="citazione">&quot;Every morning you have two choices: continue to sleep with your dreams, or wake up and chase them.&quot;</p>
               <img class="shape" src="../assets/images/home-movation-shape-01.png">
               <h3 class="name">Kaixa Stark</h3>
               <p class="firma">wingman</p>
           </div>
        </div>
      </div>
   </section>
</template>

<style lang="scss">

#about-me {
    width: 100%;
    max-width: 100%;

    .container {
        width: 80%;
        margin: 0 auto;

        .row {
            @include flex (space-between, center);
            padding: 30px 0px;

            .column {
                margin: 0px 30px;
            }

        }

        .how-to-be {
          width: 55%;

            h3 {
                color: $secondary-color;
                font-weight: bold;
                padding: 20px 0px;
                font-size: 12px;
            }
            p {
                width: 60%;
                font-weight: lighter;
                font-size: 30px;
                line-height: 1.6; 
                letter-spacing: 1px; 
            }
        }
        .want-to-learn {
            width: 50%;
            
            .introduction-text {
                font-size: 16px;
                padding: 10px 0px;
                font-weight: bold;
                line-height: 1.7;

                .text-color {
                    color: $secondary-color;
                }
            }
            .other-text {
                    font-size: 14px;
                     color: $link-color;
                     line-height: 1.6;
                }
         }
        .video {
            position: relative;
            width: 600px;
            height:350px;
            box-shadow: -9px 47px 33px -8px rgba(0,0,0,0.42);

            .img-video {
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: top;
            }
            .youtube {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate( - 50%);
            }
        }
        .cit {
            width: 30%;
            
            .citazione {
                font-size: 18px;
                line-height: 1.9;
                text-indent: -0.1rem;
            }
            .shape {
                margin-top: 50px;
                width: 25px;
            }

            .name {
                margin-top: 15px;
                font-weight: lighter;
                font-weight: bold;
            }
            .firma {
                color:$link-color;
                padding: 8px 2px;
                font-size: 15px;
            }

        }
    }
}
</style>