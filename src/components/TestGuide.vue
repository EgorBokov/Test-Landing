<template>
    <div class="test-guide">
        <div class="head-image">
            <img class="picture" :src="require('../assets/testPNG/first.png')" />
            <img class="picture" :src="require('../assets/testPNG/second.png')" />
            <img class="picture" :src="require('../assets/testPNG/third.png')" />
        </div>
        <div class="content">
        <div class="wrapper">
                <div class="header_btn">Тестовый гайд</div>
                <h2>Попробуйте наш тестовый гайд</h2>
                <p>Тестовый гайд включает в себя несколько бесплатных образов от нашего стилиста и ссылки на вещи из образов</p>
                <div class="btn">скачать гайд</div>
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
            height: 20px;
            position: absolute;
            left: 50%;
            top: -20px;
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
        }
    
            .wrapper {
                display: flex;
                flex-direction: column; 
                align-items: center;
            }

            .header_btn {
                background: #D2D2D2;
                border-radius: 3px;
                font-weight: 600;
                font-size: 14px;
                line-height: 14px;
                color: #FEFEFE;
                min-width: 123px;
                padding: 7px 0 9px;
                margin-bottom: 32px;
            }

            .btn {
                background: #000000;
                border: 1px solid #000000;
                box-sizing: border-box;
                box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
                border-radius: 5px;
                font-size: 12px;
                line-height: 12px;
                color: #FEFEFE;
                padding: 18px 0 20px;
                min-width: 122px;
            }

            h2 {
                margin: 0 0 22px;
            }

            p {
                margin-top: 0 0 32px;
            }

             
     
    }

       
</style>