<template>
  <div class="w-full h-full account">
    <div class="account-container">
      <div class="flex part-1">
        <Card :title="'Your balance'" :price="'0'" :footer-text="'0 TEDDINU'" />
        <div class="mg-card">
          <Card :title="'APY'" :price="'383,025.8%'" :footer-text="'Daily ROI 2.28%'" />
        </div>
        <Card :title="'Next Rebase'" :price="'00:08:01'" :footer-text="'Rebasing...'" />
      </div>
      <!-- <div class="table">
        <div class="table-container">
          <div v-for="(item, index) of data" :key="index" class="flex line">
            <div class="title">{{ item.title }}</div>
            <div class="value" :class="index === 1 ? 'mg-top' : ''">{{ item.value }}</div>
          </div>
        </div>
      </div> -->
      <div class="table-img">
        <img src="~/static/images/account-img.png" alt="">
      </div>
    </div>
  </div>
</template>

<script>
import Card from '~/components/Account/Card.vue';
export default {
  components: { Card },
  data() {
    return {
      data: [
        {
          title: 'Current TEDDINU Price',
          value: '$13.24'
        },
        {
          title: 'Next Reward Amount',
          value: '0 TEDDINU'
        },
        {
          title: 'Next Reward Amount USD  ',
          value: '$0'
        },
        {
          title: 'Next Reward Yield',
          value: '0.02355%'
        },
        {
          title: 'ROI(1-Day Rate) USD',
          value: '$0'
        },
        {
          title: 'ROI(5-Day Rate)',
          value: '11.96%'
        },
        {
          title: 'ROI(5-Day Rate) USD',
          value: '$0'
        },
      ]
    }
  }

}
</script>

<style lang="scss" scoped>
.account {
  .account-container {
    padding: 30px 50px;

    .mg-card {
      margin: 0 20px;
    }
  }

  .table-img {
    padding-top: 33px;
  }

  .table {
    width: 100%;

    .table-container {
      background-image: url(~/static/images/bg-account.png);
      background-repeat: no-repeat;
      background-size: contain;
      font-weight: 400;
      font-size: 24px;
      line-height: 33px;
      width: 90%;
      color: #000000;

      .line {
        border-bottom: solid 2px #000000;
        width: 90%;
        margin: 0 auto;
      }

      .title {
        width: 70%;
        padding: 12px 16px 5px px 25px;
        margin-top: 17px;
      }

      .value {
        width: 30%;
        background: #D9D9D9;
        padding: 35px 20px 5px 30px;
        text-align: center;
      }

      .mg-top {
        margin-top: 17px;
      }
    }
  }
}
</style>