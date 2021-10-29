<template>

<div class="catalogue">
    <h2>Каталог гайдов</h2>
        <div class="catalogueGrouper">
            <SubCatalogue v-for="item in catalogue"  :key="item.id" :item="item" />
        </div>
</div>

</template>

<script>

import SubCatalogue from './SubCatalogue'

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
                    image: 'mainimg.png',
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
                    image: 'mainimg.png',
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
                    image: 'mainimg.png',
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
                    image: 'mainimg.png',
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

    .catalogue {
            max-width: 1290px;
            margin: 0 auto;

                h2 {
                    font-weight: bold;
                    font-size: 32px;
                    line-height: 32px;
                    text-align: center;
                    color: #1D1D20;
                    margin: 0;
                    text-align: left;
                    margin-bottom: 50px;
                }

                .catalogueGrouper {
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    flex-wrap:  wrap;
                    max-width: 1290px;
                }
    }

</style>