<template>
    <div class="SubCatalogue">
        <div class="guideType">
            {{ item.guideType }}
        </div>
        <div class="mainImg">
            <img :src="require(`../assets/catalogueIMG/${item.image}`)" />
        </div>
        <div class="wrapper">
                <h2>{{ item.title }} </h2>
                <p>{{ item.description }}</p>
            <div class="more"><p>Читать ещё</p></div>
            <div class="svgSize">
                <div class="svgFlex">
                    <div class="svgList" v-for="svg in item.svgArray" :key="svg.id">
                        <img :src="require(`../assets/guidesSvg/${svg.icon}`)" />
                        <p>{{ svg.title }}</p>
                    </div>
                </div>
            </div>
                <div class="block_bottom">
                    <div class="button">смотреть гайд</div>
                    <p> {{ item.price }}₽ /мес.</p> 
                </div>
    
        </div>
    </div>

</template>

<script>

export default {
        name: 'SubCatalogue',
        props: {
            item: Object,
        }
    }
</script>

<style lang="scss" scoped>

.SubCatalogue {
    max-width: 620px; 
    background: #F9F9F9;
    border-radius: 15px;
    margin-bottom: 80px;
    position: relative;
    padding-bottom: 60px;

        &:nth-of-type(2) {
            .guideType {
                background-color: #638DF8;
            }
        }

        &:last-of-type {
            .guideType {
                background-color: #F16F6F;
            }
        }

        .guideType {
            position: absolute;
            top: 60px;
            left: 60px;
            background: #F5A759;
            border-radius: 3px;
            font-weight: 600;
            color: #FEFEFE;
            padding: 7px 0 9px;
            width: 98px;
        }

    .wrapper { 
        padding: 0 60px;
        max-width: 620px;

                .more {
            text-align: left;

                > p {
                    display: inline-block;
                    border-bottom: 1px dotted #A6A6A6;
                    font-weight: normal;
                    font-size: 15px;
                    line-height: 15px;
                }
            }
    }

    

    .svgSize {
        height: 168px;

            .svgList {
                display: flex;
                flex-direction: row;
                align-items: center;

            img {
                margin-right: 16px;
            }
        }
    }

    
    h2 {
        margin-bottom: 18x;
        text-align: left;

        +p {
            margin-bottom: 14px;
            max-width: 450px;
            text-align: left;
        }
    }

    
    .block_bottom {
        display: flex;
        align-items: center;
        justify-content: space-between;
        max-width: 500px;
        margin: 0 auto;
        
            &:last-child {
                font-size: 26px;
                line-height: 26px;
                color: #1D1D20;
            }

            .button {
                padding: 18px 40px 20px;
                border: 1px solid black;
                border-radius: 10px;
                font-size: 12px;
                line-height: 12px;
                color: #000000;
            }

        
    }
}
</style>