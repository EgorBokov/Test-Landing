<template>
    <div class="test-guide">
        <div class="head-image">
            <img class="picture" :src="require('../../assets/images/png/clothes/first.png')" />
            <img class="picture" :src="require('../../assets/images/png/clothes/second.png')" />
            <img class="picture" :src="require('../../assets/images/png/clothes/third.png')" />
        </div>
        <div class="content">
            <div class="wrapper">
                <div class="header-btn">
                    Тестовый гайд
                </div>
                 <h2>Попробуйте наш тестовый гайд</h2>
                    <p>Тестовый гайд включает в себя несколько бесплатных образов от нашего стилиста и ссылки на вещи из образов</p>
                        <div class="bottom-btn">
                        скачать гайд
                        </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TestGuide',
    props: {},
}
</script>

<style lang="scss" scoped>

.test-guide {
    position: relative; 
    max-width: 1290px;
    margin: 200px auto 80px;
    border: 1px solid #1D1D20;
    border-radius: 20px;

        &::after {
            content: '';
            width: 200px;
            height: 75px;
            position: absolute;
            left: 50%;
            top: -43px;
            transform: translateX(-50%);
            background: #fff;
        }
        
        .head-image {
            position: absolute; 
            transform: translateY(-50%) translateX(-50%);
            left: 50%;
            max-width: 300px;
            z-index: 1000;

                .picture {
                    width: 100px;
                    height: 100px;
                    padding: 0;
                }
        }

        .content {
            margin: auto;
            max-width: 500px;
            padding: 110px 0px 100px;

            .wrapper {
                text-align: center;

                .header-btn {
                    background: #D2D2D2;
                    border-radius: 3px;
                    font-weight: 600;
                    font-size: 14px;
                    line-height: 14px;
                    color: #FEFEFE;
                    max-width: 123px;
                    padding: 7px 0 9px;
                    margin: 0 auto;
                    margin-bottom: 32px;
                }

                 h2 {
                    margin: 0 auto 22px;
                    font-weight: bold;
                    font-size: 32px;
                    line-height: 32px;
                }

                p {
                    margin: 0 auto 32px;
                    font-size: 17px;
                    line-height: 22px;
                }

                .bottom-btn {
                    background: #000000;
                    border: 1px solid #000000;
                    box-sizing: border-box;
                    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
                    border-radius: 5px;
                    font-size: 12px;
                    line-height: 12px;
                    color: #FEFEFE;
                    margin: 0 auto;
                    padding: 18px 20px;
                    max-width: 122px;
                }
            }
        }

}

       
</style>