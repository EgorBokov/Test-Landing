<template>
  <div class="main-head">
    <div class="content">
      <h1>Обновлять гардероб теперь легко и удобно</h1>
      <p>Это подборки образов из самых популярных и наиболее сочетаемых товаров, выпущенных в продажу в этом месяце.</p>
        <div class="button">
          перейти к каталогу
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
  },
}
</script>

<style lang="scss" scoped>

  $main-color: #FFFFFF;

  .main-head {
    background-size: cover;
    background-image: url('../../assets/images/png/main-images/main-head-img.png');
    border: 1px solid black;
    border-radius: 0px 0px 150px 0px;
    min-height: 540px;
    color: $main-color;

      .content {
          margin-top: 149px;

            h1 {
                font-weight: bold;
                font-size: 40px;
                line-height: 45px;
                text-align: center;
                max-width: 600px;
                height: 90px;
                margin: 0 auto;
                margin-bottom: 22px;
              }

            p {
                max-width: 600px;
                min-height: 48px;
                font-size: 17px;
                line-height: 24px;
                text-align: center;
                margin: 0 auto;
                margin-bottom: 32px;
              }

            .button {
                padding: 18px 0px 20px;
                margin: 0 auto;
                font-size: 12px;
                line-height: 12px;
                color: #FEFEFE;
                text-align: center;
                background: #1D1D20;
                border-radius: 5px;
                max-width: 200px;
              }
        }
  }

    
     
</style>

