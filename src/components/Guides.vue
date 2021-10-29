<template>
<div class="guides-wrapper">
    <div class="guides">
        <h2>Какие образы будут в гайде?</h2>
        <p class="description">Это подборки образов из самых популярных и наиболее сочетаемых товаров, выпущенных в продажу в этом месяце.</p>
        <Guide v-for="guide in guides" :key="guide.guideType" :guide="guide"/>
    </div>
</div>
</template>

<script>
import Guide from "./Guide"

export default {
  name: 'Guides',
  data() {
      return {
          guides: [
              {
                  title: 'Гайд с повседневными образами',
                  subTitle: '25+ готовых образов из миддл, люкс и лучших российских брендов, а также 10 образов с эксклюзивными моделями кроссовок',
                  mainPic: 'firstPic',
                  imageryNum: '25+',
                  guideType: 'Макси гайд',
                  mainImage: 'mainFirst.png',
                  svgArray: [
                      {title: 'Закрытый чат со стилистом', path: 'telegram.svg' },
                      {title: 'Фото и видео с лайв-примерок', path: 'camera.svg' },
                      {title: 'Промокод на 15%  на покупки', path: 'star.svg' },
                      ],
                  clothes: [
                        {title: 'Off-White', description: 'Тренч с принтом', path: 'trench.png',},
                        {title: 'Danielle Guizio', description: 'платье мини со сборками и вырезом', path: 'dress.png',},
                        {title: 'Gentle Monster', description: 'солнцезащитные очки Bibi', path: 'glasses.png',},
                    ],
                }, 
              {
                  title: 'Гайд с повседневными образами',
                  subTitle: '20+ готовых образов из миддл, масс-маркет и лучших российских брендов, а также 10 образов с эксклюзивными моделями кроссовок, с указанием артикулов, стоимости и ссылки на каждую вещь',
                  mainPic: 'firstPic',
                  imageryNum: '20+',
                  guideType: 'Мини гайд',
                  mainImage: 'mainSecond.png',
                  svgArray: [
                      {title: 'Закрытый чат со стилистом', path: 'telegram.svg' },
                      {title: 'Фото и видео с лайв-примерок', path: 'camera.svg' },
                      {title: 'Промокод на 15%  на покупки', path: 'star.svg' },
                      ],
                  clothes: [
                        {title: 'Zara', description: 'Трикотажный Кардиган', path: 'jacket.png',},
                        {title: 'Zara', description: 'Брюки из вильвета', path: 'trousers.png',},
                        {title: 'H&M', description: 'Футболка Оверсайз', path: 'tshirt.png',},
                        {title: 'Air Jordan', description: 'SE Multi-Color', path: 'sneakers.png',},
                    ],
              },
              ],
      }
  },
  components: {
      Guide,
  }
}
</script>

<style lang="scss" scoped>
.guides-wrapper {
    background: #F9F9F9;
    
    .guides {
        max-width: 1291px;
        margin: 0px auto;
        border-radius: 150px 0px 0px 0px;
        padding: 160px 0px 80px;

        
        .description {
            max-width: 600px;
            margin: 0px auto 60px;
        }
    }
}


</style>
