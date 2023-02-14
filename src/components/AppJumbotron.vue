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
                <button type="text" class="get-started">
                    Get Started For Free 
                    <font-awesome-icon icon="fa-solid fa-arrow-right-long" />
                </button>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

#jumbotron {
    width: 100%;
    max-width: 100%;

    .container {
        width: 80%;
        margin: 0 auto;
        padding: 100px 0px;

        .text {
            font-size: 15px;
            padding: 10px 0px;
        }
        .large-text {
                font-weight: lighter;
                font-size: 50px;
                line-height: 1.4; 
                letter-spacing: 1px; 
                 padding: 0px 10px;
            }
    }
}
</style>