<template>
  <div class="flex w-full h-full relative justify-between dashboard">
    <div class="w-full h-full dashboard-container">
      <div class="flex px-4">
        <div class="partern flex flex-col">
          <div class="intro">
            <div class="title-intro">
              Market value of treasure
            </div>
            <div class="price-intro">
              $1,689,496
            </div>
          </div>
          <Card :title="'Total Supply'" :price="'$1,689,496'" />
          <Card :title="'Circulating Supply'" :price="'4,738,612.27'" />
          <Card :title="'# Value of FirePit'" :price="'$1,689,496'" />
        </div>
        <div class="partern flex flex-col">
          <div class="teddu-price">
            <div class="teddu-price_container">
              <div class="teddu-price_title">
                Teddinu price
              </div>
              <div class="teddu-price_content">
                <div class="teddu-price_price">
                  $12.92
                </div>
                <div class="teddu-price_clock">
                  <span class="text-pd">00 : 00 :00</span>
                </div>
                <div class="teddu-price_footer">
                  Rebasing...
                </div>
              </div>
            </div>
          </div>
          <Card :title="'$ Value of FirePit'" :price="'$1,689,496'" />
        </div>
        <div class="partern flex flex-col">
          <div class="intro">
            <div class="title-intro">
              Teddinu inssurent fund value
            </div>
            <div class="price-intro">
              $1,068,839
            </div>
          </div>
          <Card :title="'MarketCap'" :price="'$1,689,496'" />
          <Card :title="'Pool Value'" :price="'$1,689,496'" />
          <Card :title="'% FirePit : Supply'" :price="'$1,689,496'" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from '~/components/Dashboard/Card.vue';
export default {
  components: { Card }
}
</script>

<style lang="scss" scoped>
.dashboard-container {
  padding: 0 30px;

  .intro {
    margin: 40px 0;
    text-align: center;

    .title-intro {
      font-weight: 400;
      font-size: 32px;
      color: #FFFFFF;
    }

    .price-intro {
      color: #3DFF39;
      font-weight: 400;
      font-size: 40px;
    }
  }

  .teddu-price {

    margin-top: 35px;

    &_container {
      background-image: url(~/static/images/bg-clock.png);
      background-repeat: no-repeat;
      background-size: cover;
      width: 427px;
      height: 533px;
      position: relative;
    }

    &_content {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100%;
    }

    &_title {
      background-image: url(~/static/images/bg-title.png);
      background-repeat: no-repeat;
      background-size: cover;
      width: 464px;
      height: 79px;
      text-align: center;
      line-height: 80px;
      font-size: 32px;
      color: #FFF2F2;
      position: absolute;
      right: -20px;
      top: 17px;
    }

    &_clock {
      background-image: url(~/static/icons/clock.png);
      background-repeat: no-repeat;
      background-size: contain;
      width: 371px;
      height: 167px;
      margin: 0 auto;
      font-weight: 400;
      font-size: 64px;
      line-height: 145px;
      text-align: center;
      color: #FFFFFF;
      margin-left: 35px;

      .text-pd {
        display: inline-block;
        padding-right: 20px;
      }
    }

    &_price {
      font-weight: 400;
      font-size: 40px;
      color: #000000;
      padding: 16px 0 50px 0;
      text-align: center;
      margin-top: 40px;
    }

    &_footer {
      text-align: center;
      font-size: 32px;
      color: #000000;
      padding: 26px 0 20px 0;
    }
  }
}

.card {
  margin: 15px 5px;
}

.partern {
  margin: 0 15px;
}
</style>