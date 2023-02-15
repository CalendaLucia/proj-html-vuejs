<script>
export default {
    name:'AppFooter',
    data() {
        return {

            
        }
    },
    props: {
       address: {
            type: Array,
            required: true,
       },

       social: {
            type: Array,
            required: true,
       },

       explore: {
            type: Array,
            required: true,
       },

       information: {
        type:Array,
        required:true,
       }

     },
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="row left">
                <div class="column">
                    <ul class="group-list">
                        <li v-for="(item, index) in address" :key="item.id" :class="index === 0 ? 'title' : ''">
                            {{ item.label }}
                        </li>
                    </ul>
                    <ul class="group-list group-icons">
                        <li class="item-icons" v-for="icon in social">
                            <font-awesome-icon :icon="icon.icon" class="icon"/>
                        </li>
                    </ul>
                </div>
                <div class="row right">
                    <div class="column">
                      <ul class="group-list group-explore">
                        <li class="item-explore" v-for="(item, index) in explore" :key="item.id" :class="index === 0 ? 'title' : ''">
                            {{ item.label }}
                        </li>
                      </ul>
                    </div>
                    <div class="column">
                       <ul class="group-list group-information">
                          <li class="item-info" v-for="(item, index) in information" :key="item.id" :class="index === 0 ? 'title' : ''">
                             {{ item.label }}
                          </li>
                       </ul>
                    </div>
                </div>
            </div>
            <div class="reserved">
                <p> <span>&reg;</span>2020 Maxcoach.All Rights Reserved</p>
                <div class="circle">
                    <font-awesome-icon class="arrow-up" icon="fa-solid fa-arrow-up-long"/>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    background-color: #171621;
    width: 100%;
    padding: 30px 0px;
    position: relative;

    .container {
        width: 80%;
        margin: 0 auto;
        .group-list {
                    list-style: none;
                    color: #9a9a9b;
                    font-size: 12px;
                    line-height: 2.5;

                    .title {
                        color: $primary-color;
                        font-size: 15px;
                        font-weight: bold;                 
                    }

                }

        .left {
            width: 100%;
            @include flex (space-between, baseline);

            .column:first-child {
                width: 40%;
               
                    .item-icons {
                        display: inline-block;
                        padding-top: 20px;
                        .icon {
                            font-size: 20px;
                                               
                        }
  
                    }
                
                .group-icons {
                    width: 40%;
                    @include flex (space-between,center)
                    
                }

            }

            
        }

        .reserved {
            width: 100%;
            @include flex (center, center);
            padding-top: 30px;
            color: #9a9a9b;
            font-weight: bold;
            font-size: 15px;
             
              p span {
                font-size: 24px;
             }

             .circle {
                width: 60px;
                height: 60px;
                border-radius: 50%;
                background-color: $secondary-color;
                position: relative;
                position: absolute;
                bottom: 0px;
                right: 0px;
                z-index: 1;

                
             
                 .arrow-up {
                    color: white;
                    font-size: 25px;
                    position: absolute;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    z-index: 2;
                 }
                
             }
        }

        .right {
            @include flex (center, baseline);
            width: 60%;

            .group-explore {
                    display: flex;
                    flex-direction: column;
                    flex-wrap: wrap;
                    height: 140px;

                    .item-explore:nth-child(5) {
                        margin-top: 36px;
                        
                    }
                }

                .group-information {
                    margin-left: 50px;
                    width: 100%;
                     
                }
        }
    }
}
</style>