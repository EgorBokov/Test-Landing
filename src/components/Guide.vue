<template>
  <div class="guide">
        <div class="content">
            <div class="type">{{guide.guideType}}</div>
            <h3 class="title"> {{ guide.title }} </h3>
            <p class="subTitle">{{ guide.subTitle }}</p>

            <div class="svgBlock" v-for="svg in guide.svgArray" :key="svg.title">
                <img :src="require(`../assets/guidesSvg/${svg.path}`)" />
                <p class="svgTitle">{{svg.title}}</p>
            </div>

            <div class="clothes_wrapper">
                <div class="clothes" v-for="item in guide.clothes" :key="item.title">
                    <img :src="require(`../assets/clothesPNG/${item.path}`)" />
                    <h4>{{item.title}}</h4>
                    <p>{{item.description}}</p>
                </div>
            </div>

        </div>

        <div class="image">
            <img :src="require(`../assets/clothesPNG/${guide.mainImage}`)" />
                <div class="imagery">
                    <div>{{ guide.imageryNum }} </div>
                    <div>образов</div>
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
.guide {
    display: flex;
    justify-content: space-between;

    .type {
        max-width: 130px;
        font-weight: 600;
        font-size: 14px;
        line-height: 14px;
        color: #FEFEFE;
        padding: 7px 14px 9px;
        background: #F16F6F;
        border-radius: 3px;
        margin-bottom: 40px;
    }

    .title {
         margin-top: 0;
         margin-bottom: 18px;
         text-align: left;
    }

    .subTitle {
        margin-bottom: 32px;
        max-width: 500px;
        text-align: left;
    }

    .clothes_wrapper {
    display: flex;
    margin-top: 133px;
    margin-bottom: 117px;

    .clothes {
        width: 150px;
        margin: 0px 20px 5px 0px;
        text-align: left;

            &:last-child {
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
    
        .type {
            background-color: #638DF8;
        }
    }
}


.guide:last-of-type > div:last-child{
    order: 1;

    
    .imagery {
        background-color: #638DF8;
    }
}

.image {
    position: relative;
}

.svgBlock {
    display: flex;
    justify-content: flex-start;

    p {
        margin-left: 16px;
    }
}

.imagery {
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








</style>

