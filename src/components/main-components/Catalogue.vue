<template>
<div class="main-catalogue">
    <h2>Каталог гайдов</h2>
        <div class="catalogue-list">
            <SubCatalogue v-for="item in catalogue"  :key="item.id" :item="item" />
        </div>
</div>
</template>

<script>

import SubCatalogue from '../sub-components/SubCatalogue'

export default {
    name: 'Catalogue',
    components: {
        SubCatalogue,
        },
    data() {
        return {
            catalogue: [
                {   
                    id: 0,
                    guideType: 'Мини гайд',
                    image: 'main-catalogue.png',
                    title: 'Спортивный гайд',
                    description: '25+ готовых образов из масс-маркет брендов, с указанием артикулов, стоимости и ссылки на каждую вещь ( Zara, Uniqlo, H&M, Mango, ASOS, Stradivarius, La sarcelle и многие другие ).',
                    price: 800,
                    svgArray: [
                        { icon: 'telegram.svg', title:'Закрытый чат со стилистом'},
                        { icon: 'star.svg', title:'Промокод на 15%  на покупки'}
                    ],
                },
                {
                    id: 1,
                    guideType: 'Миди гайд',
                    image: 'main-catalogue.png',
                    title: 'Спортивный гайд',
                    description: '25+ готовых образов из масс-маркет брендов, с указанием артикулов, стоимости и ссылки на каждую вещь ( Zara, Uniqlo, H&M, Mango, ASOS, Stradivarius, La sarcelle и многие другие ).',
                    price: 1200,
                    svgArray: [
                        { icon: 'telegram.svg', title:'Закрытый чат со стилистом'},
                        { icon: 'camera.svg', title:'Фото и видео с лайв-примерок'},
                        { icon: 'star.svg', title:'Промокод на 15%  на покупки'}
                    ],
                },
                {
                    id: 2,
                    guideType: 'Мини гайд',
                    image: 'main-catalogue.png',
                    title: 'Спортивный гайд',
                    description: '25+ готовых образов из масс-маркет брендов, с указанием артикулов, стоимости и ссылки на каждую вещь ( Zara, Uniqlo, H&M, Mango, ASOS, Stradivarius, La sarcelle и многие другие ).',
                    price: 800,
                    svgArray: [
                        { icon: 'telegram.svg', title:'Закрытый чат со стилистом'},
                        { icon: 'star.svg', title:'Промокод на 15%  на покупки'}
                    ],
                },
                {
                    id: 3,
                    guideType: 'Макси гайд',
                    image: 'main-catalogue.png',
                    title: 'Спортивный гайд',
                    description: '25+ готовых образов из масс-маркет брендов, с указанием артикулов, стоимости и ссылки на каждую вещь ( Zara, Uniqlo, H&M, Mango, ASOS, Stradivarius, La sarcelle и многие другие ).',
                    price: 1600,
                    svgArray: [
                        { icon: 'telegram.svg', title:'Закрытый чат со стилистом'},
                        { icon: 'camera.svg', title:'Фото и видео с лайв-примерок'},
                        { icon: 'star.svg', title:'Промокод на 15%  на покупки'}
                    ],
                },
            ],         
        }
    }
}
</script>

<style lang="scss" scoped>

    .main-catalogue {
            max-width: 1290px;
            margin: 0 auto;

                h2 {
                    font-weight: bold;
                    font-size: 32px;
                    line-height: 32px;
                    text-align: center;
                    margin: 0;
                    text-align: left;
                    margin-bottom: 50px;
                }

                .catalogue-list {
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    flex-wrap:  wrap;
                    max-width: 1290px;
                }
    }

    @media all and (max-width: 375px) {
        .main-catalogue {
            max-width: 360px;
            

                h2 {
                    font-size: 22px;
                    line-height: 22px;
                    margin-bottom: 22px;
                }

                .catalogue-list {
                    flex-direction: column;
                }
    }
    }

</style>