<template>
  <div class="MainAvert">
    <div class="main-head">
      <div class="content">
        <h1>Обновлять гардероб теперь легко и удобно</h1>
        <p>Это подборки образов из самых популярных и наиболее сочетаемых товаров, выпущенных в продажу в этом месяце.</p>
          <div class="butt">перейти к каталогу</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style lang="scss" scoped>

    .main-head {
      background-image: url('../assets/main-head.png');
      border: 1px solid black;
      border-radius: 0px 0px 150px 0px;
      min-height: 540px;

       .content {
        margin-top: 149px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

          h1 {
                font-weight: bold;
                font-size: 40px;
                line-height: 45px;
                text-align: center;
                color: #FFFFFF;
                max-width: 600px;
                height: 90px;
                margin-bottom: 22px;
              }

          p {
              max-width: 600px;
              min-height: 48px;
              font-size: 17px;
              line-height: 24px;
              text-align: center;
              color: #FFFFFF;
              margin-bottom: 32px;
            }

        .butt {
                margin: 0 860px;
                width: 200px;
                height: 50px;
                font-size: 12px;
                line-height: 12px;
                color: #FEFEFE;
                background: #1D1D20;
                border-radius: 5px;
                text-align: center;
                display: flex;
                align-items: center;
                justify-content: center;
              }
      }
    }

    
     
</style>

