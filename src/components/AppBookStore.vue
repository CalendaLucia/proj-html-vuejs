<script>
export default {
    name: 'AppBookStore',
    data() {
        return {
            
        }
    },
}
</script>

<template>
   <section id="store">
      <div class="container">
         <div class="description">
             <p class="text">BOOK STORE ONLINE</p>
             <p class="other-text">Be Alpha With 
                <span class="text-color">Wingman's Book</span> </p>
             <ul class="group-list">
                <li>
                    <font-awesome-icon class="icon" icon="fa-solid fa-check" />
                    Help you understand yourself better
                </li>
                <li>
                    <font-awesome-icon class="icon" icon="fa-solid fa-check" />
                    Revealing mature tips
                </li>
                <li>
                    <font-awesome-icon class="icon" icon="fa-solid fa-check" />
                     Give the right advice
                </li>
                <li>
                    <font-awesome-icon class="icon" icon="fa-solid fa-check" />
                     Fascinating examples of alpha man
                </li>
             </ul>
             <div class="get-free-book">
               <button type="text" class="start">
                  Get Free Ebook
               </button>
        </div>
         </div>
         <div class="books">
            <div class="cover">
                <img src="../assets/images/product-book-11-400x400.jpg">
                <h5>Alpha man by Maxcoach</h5>
                <p class=" text-color">$29.00</p>
                <div class="overlay">
                  <div class="icons">
                     <font-awesome-icon class="icon" icon="fa-solid fa-magnifying-glass"/>
                     <font-awesome-icon class="icon" icon="fa-solid fa-cart-shopping"/>
                     <font-awesome-icon class="icon" icon="fa-regular fa-heart"/>
                     <font-awesome-icon class="icon" icon="fa-solid fa-signal"/>
                  </div>
                </div>
            </div>
            <div class="cover">
                <img src="../assets/images/product-book-10-400x400.jpg">
                <h5>Real man 4.0 by Maxcoach</h5>
                <p class="text-color">$39.00</p>
                <div class="overlay">
                  <div class="icons">
                     <font-awesome-icon class="icon" icon="fa-solid fa-magnifying-glass"/>
                     <font-awesome-icon class="icon" icon="fa-solid fa-cart-shopping"/>
                     <font-awesome-icon class="icon" icon="fa-regular fa-heart"/>
                     <font-awesome-icon class="icon" icon="fa-solid fa-signal"/>
                  </div>
                </div>
            </div>
         </div>
         <div class="logos">
            <div class="logo">
                <img src="../assets/images/client-logo-05-primary.png">
            </div>
            <div class="logo">
                <img src="../assets/images/client-logo-06-primary.png">
            </div>
            <div class="logo">
                <img src="../assets/images/client-logo-01-primary.png">
            </div>
            <div class="logo">
                <img src="../assets/images/client-logo-04-primary.png">
            </div>
            <div class="logo">
                <img src="../assets/images/client-logo-03-primary.png">
            </div>
            <div class="logo">
                <img src="../assets/images/client-logo-02-primary.png">
            </div>
         </div>
      </div>
   </section>
</template>

<style lang="scss" scoped>

#store {
    width: 100%;

    .container {
        width: 80%;
        margin: 0 auto;
        @include flex (space-between, center);
        flex-wrap: wrap;

        .description {
            line-height: 1.4;
             width:30%;
            
            .text {
                font-size: 15px;
                padding: 20px 0px;
            }
            .other-text {
                    color: $hover-button-color;
                    font-size: 30px;
                    font-weight: lighter;

                    .text-color {
                        color: $secondary-color;
                    }
              }

              .group-list {
                 list-style: none;
                 padding-top: 20px;

                 li {
                  color: $link-color;
                  font-size: 12px;
                  line-height: 2.4;
              

                  .icon {
                    color: $secondary-color;
                     font-size: 15px;
                     padding: 5px 5px;
                     vertical-align:middle ;
                  }
                 }
            
            }

            .get-free-book {
                 padding-top: 30px;
                .start {
                   padding: 15px 40px;
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

        .books {
            width: 70%;
            @include flex (center, center );

            .cover {
                width: 40%;
                margin: 0px 10px;
                text-align: center;
                font-weight: lighter;
                position: relative;

               
                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }

                h5 {
                    font-size: 15px;
                     padding: 10px 0px;
                }

                .text-color {
                    color: $secondary-color;
                    font-size: 20px;
                }
                  .overlay {
                     width: 100%;
                     height: 100%;
                     position: absolute;
                     top: 0px;
                     left: 0px;
                     background-color: rgba(0,0,0,0.1);
                     display: none;


                     .icons {
                        @include flex (center, flex-end);
                        flex-direction: column;
                        margin: 30px 20px;
                      

                        .icon {
                             font-size: 15px;
                             background-color: white;
                             border-radius: 50%;
                             padding: 15px 15px;
                             margin: 10px 5px;
                        }
                       
                     }
                }
                
            }
            .cover:hover .overlay {
               display: block;
               
}

         
                

        
         
        }

        .logos {
            width: 100%;
            @include flex (space-around,center);
            padding: 130px 0px;

            .logo {

                img {
                    filter: grayscale(100%);
                }
            }
        }
    }
}
</style>
