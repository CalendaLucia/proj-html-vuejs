<script>
export default {
    name:'AppJumbotron',data() {
        return {
            
        }
    },

}
</script>

<template>
    <section id="jumbotron">
        <div class="container">
            <div class="get-started">
                <p class="text">I'M WINGMAN</p>
                <h1 class="large-text">Peace On Earth A Wonderful Wish But No Way</h1>
                <p class="other-text">Success isn't overnight. It's when everyday you get a little bettere than the day before. It all adds up.</p>
                <button type="text" class="start">
                    Get Started For Free 
                    <font-awesome-icon icon="fa-solid fa-arrow-right-long" />
                </button>
            </div>
            <div class="box-image">
                <img src="../assets/images/home-movation-hero-image.png">
            </div>
            <div class="icons">
                <img class="myicon" src="../assets/images/ruler.png">
                <img class="myicon" src="../assets/images/lifebuoy.png" >
                <font-awesome-icon class="myicon" icon="fa-solid fa-book"/>
                <font-awesome-icon class="myicon" icon="fa-solid fa-cart-shopping"/>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

#jumbotron {
    width: 100%;
    max-width: 100%;
    position: relative;

    .container {
        width: 80%;
        margin: 0 auto;
        padding-top: 50px;
        @include flex (space-between, center);

        .text {
            font-size: 15px;
            padding: 10px 0px;
        }
        .large-text {
                width: 80%;
                font-weight: lighter;
                font-size: 50px;
                line-height: 1.2; 
                letter-spacing: 1px; 
            }
        .other-text{
             width: 80%;
             padding: 20px 0px;
             font-weight: lighter;
             color: $link-color;
             line-height: 2.1; 
        }

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

        .box-image {
            width: 80%;
            background-image: url('../assets/images/home-movation-shape-face-big.png');
            background-repeat: no-repeat;
            background-size: contain;
            background-position: center;
            align-self: flex-end;

            img {
                width: 100%;
                object-fit: cover;
                align-self: flex-end;
            }
        }

        .icons {
            position: absolute;
            right: 10px;
            top: 100px;
            display: flex;
            flex-direction: column;
            padding: 0px 10px;
            background-color: $primary-color;
              .myicon {
                 width: 15px;
                 margin: 10px 0px;
                
             }

        }

    }

  
}


</style>