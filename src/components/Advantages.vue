<template>
    <div class="centerer">
      <div class="main">
            <h1>Преимущества гайдов</h1>
            <p>Это подборки образов из самых популярных и наиболее сочетаемых товаров, выпущенных в продажу в этом месяце.</p>
            <div class="container">
                <SubAdvantages v-for="ad in adList" :key="ad.id" :ad="ad"/>
            </div>
        </div>
    </div>
</template>

<script>
import SubAdvantages from "./SubAdvantages.vue"

export default {
    name: 'Advantages',
    props: {},
    components: {
        SubAdvantages,
    },
    data() {
        return {
            adList: [
                {id: 0, icon: 'mainTime.svg', title: 'Экономия времени', text: 'Гайд содержит в себе стильные образы, состоящие из вещей, которые сочетаются между собой'},
                {id: 1, icon: 'actual.svg', title: 'Актуальные образы', text: 'Наш стилист регулярно обновляет гайды, чтобы вы всегда выглядели стильно и актуально'},
                {id: 2, icon: 'study.svg', title: 'Обучение', text: 'Вы не только пользуетесь готовыми образами, но и учитесь у опытного стилиста искусству стиля'},
                {id: 3, icon: 'star.svg', title: 'Бонусы от Meet-market', text: 'В каждом гайде вы найдете подборку уникальных бонусов'},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

.centerer {
  margin-top: 80px;
  display:flex;
  justify-content: center;

    .main {
        max-width: 1291px;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;

            h1 {
                width: 338px;
                height: 32px;
                font-style: normal;
                font-weight: bold;
                font-size: 32px;
                line-height: 32px;
                text-align: center;
                color: #1D1D20;
                margin-bottom: 22px;
                margin-top: 0;
            }

            p {
                width: 600px;
                height: 44px;
                font-size: 17px;
                line-height: 22px;
                text-align: center;
                color: #1D1D20;
                margin-bottom: 50px;
            }

            .container {
                display: flex;
                justify-content: space-between;
            }
    }
}






</style>