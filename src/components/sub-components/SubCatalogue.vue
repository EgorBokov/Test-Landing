<template>
    <div class="main-sub-catalogue">
        <div class="guide-type">
            {{ item.guideType }}
        </div>
        <div class="main-image">
            <img :src="require(`../../assets/images/png/main-images/${item.image}`)" />
        </div>
        <div class="wrapper">
                <h2>{{ item.title }} </h2>
                <p>{{ item.description }}</p>
            <div class="title-more"><p>Читать ещё</p></div>
            <div class="svg-wrapper">
                <div class="svg-flex">
                    <div class="svg-list-block" v-for="svg in item.svgArray" :key="svg.id">
                        <img :src="require(`../../assets/images/svg/${svg.icon}`)" />
                        <p>{{ svg.title }}</p>
                    </div>
                </div>
            </div>
                <div class="block-bottom">
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

.main-sub-catalogue {
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
            .guide-type {
                background-color: #F16F6F;
            }
        }

        .guide-type {
            position: absolute;
            top: 60px;
            left: 60px;
            background: #F5A759;
            border-radius: 3px;
            font-weight: 600;
            font-size: 14px;
            line-height: 14px;
            color: #FEFEFE;
            padding: 7px 14px 9px;
            max-width: 98px;
        }

    .wrapper { 
        padding: 50px 60px 0;
        max-width: 620px;

        h2 {
            margin: 0px;

            +p {
                color: #A6A6A6;
            }
        }

        .title-more {
            text-align: left;

            p {
                display: inline-block;
                border-bottom: 1px dotted #A6A6A6;
                font-weight: normal;
                font-size: 15px;
                line-height: 15px;
                color: #A6A6A6;
            }
        }

        .svg-wrapper {
            min-height: 168px;

                .svg-list-block {
                    display: flex;
                    flex-direction: row;
                    align-items: center;

                    img {
                        margin-right: 16px;
                    }
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

    
    .block-bottom {
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
                border-radius: 5px;
                font-size: 12px;
                line-height: 12px;
                color: #000000;
            } 
    }
}

@media all and (max-width: 375px) {
    .main-sub-catalogue {
        max-width: 323px; 
        border-radius: 10px;
        margin-bottom: 32px;
        padding-bottom: 22px;

    .main-image img {
        max-width: 323px; 
    }

     .guide-type {
        top: 22px;
        left: 22px;
        padding: 6px 12px;
        max-width: 84px;
        font-size: 12px;
        font-weight: 600;
    }

    .wrapper { 
        padding: 22px 26px 0px;
        max-width: 620px;

            .title-more {

                > p {
                    font-size: 14px;
                    line-height: 14px;
                }
            }


            .svg-wrapper {
                min-height: 0px;

                    .svg-list-block {
                        align-items: center;

                        p {
                            font-size: 14px;
                            line-height: 14px;
                        }

                        img {
                            margin-right: 14px;
                        }
                    }
            }
    }

    h2 {
        margin-bottom: 12px;

        +p {
            margin-bottom: 12px;
            max-width: 279px;
        }
    }

    
    .block-bottom {
        max-width: 279px;
        flex-direction: column;
        align-items: flex-start;
        padding-bottom: 0px;
        
            &:last-child {
                font-size: 18px;
                font-weight: bold;
                line-height: 18px;
                order: 2;
            }

            .button {
                padding: 18px 90px 20px;
                border-radius: 5px;
                font-size: 12px;
                font-weight: 400;
                line-height: 12px;
                order: 1
            }
        }
    }
}
</style>