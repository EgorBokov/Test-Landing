<template>
  <div class="main-guide">
        <div class="content">
            <div class="guide-type">
                {{guide.guideType}}
            </div>
                <h3 class="guide-title"> {{ guide.title }} </h3>
                <p class="guide-subtitle">{{ guide.subTitle }}</p>

            <div class="svg-list" v-for="svg in guide.svgArray" :key="svg.title">
                <img :src="require(`../../assets/images/svg/${svg.path}`)" />
                <p class="svg-title">{{svg.title}}</p>
            </div>

            <div class="clothes-wrapper">
                <div class="clothes-list" v-for="item in guide.clothes" :key="item.title">
                    <img :src="require(`../../assets/images/png/clothes/${item.path}`)" />
                    <h4>{{item.title}}</h4>
                    <p>{{item.description}}</p>
                </div>
            </div>
        </div>
        <div class="main-image">
            <img :src="require(`../../assets/images/png/main-images/${guide.mainImage}`)" />
                <div class="imagery-num">
                    <div>
                        {{ guide.imageryNum }}
                    </div>
                        <div>
                            образов
                        </div>
                </div>
        </div>
  </div>
</template>

<script>
export default {
  name: 'Guide',
  props: {
      guide: Object,
  }
}
</script>

<style lang="scss" scoped>

.main-guide {
    display: flex;
    justify-content: space-between;

    .guide-type {
        max-width: 103px;
        font-weight: 600;
        font-size: 14px;
        line-height: 14px;
        color: #FEFEFE;
        padding: 7px 14px 9px;
        background: #F16F6F;
        border-radius: 3px;
        margin-bottom: 40px;
        text-align: center;
    }

    .guide-title {
         margin-top: 0;
         margin-bottom: 18px;
         text-align: left;
         font-weight: bold;
         font-size: 26px;
         line-height: 26px;
         max-width: 500px;
    }

    .guide-subtitle {
        margin-bottom: 32px;
        max-width: 500px;
        text-align: left;
        color: #A6A6A6;
    }

    .svg-list {
        display: flex;
        justify-content: flex-start;

            p {
                margin-left: 16px;
            }
    }

    .clothes-wrapper {
        display: flex;
        flex-wrap: wrap;
        margin-top: 123px;
        margin-bottom: 117px;
        color: #000;
        max-width: 680px;

        .clothes-list {
            width: 150px;
            margin: 10px 20px 5px 0px;
            text-align: left;

                &:last-of-type {
                    margin-right: 0;
                }

                img {
                    max-width: 100px;
                    margin-bottom: 5px;
                }

                h4 {
                    margin: 0px;
                    margin-bottom: 5px;
                }

                p {
                    margin: 0px;
                    font-size: 13px;
                }
        }
    }

    &:first-of-type{
        margin-bottom: 100px;
    }

    &:last-of-type > div:first-child{
        order: 2;
    
        .guide-type {
            background-color: #638DF8;
        }
    }

    &:last-of-type > div:last-child{
    order: 1;

        .imagery-num {
            background-color: #638DF8;
        }
    }

    .main-image {
        position: relative;

            .imagery-num {
                display: flex;
                flex-direction: column;
                justify-content: center;
                background-color: #F16F6F;
                border-radius: 100px;
                width: 138px;
                height: 138px;
                text-align: center;
                color: #FEFEFE;
                position:absolute; 
                left: 100%;
                transform: translateX(-70%);
                top: 472px;

                    > div:first-child {
                        font-weight: bold;
                        font-size: 40px;
                    }
            }
    }
}







</style>

