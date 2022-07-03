<template>
  <div class="side-bar">
    <div class="flex flex-col w-full relative banner-container">
      <div class="icon-sidebar-img">
        <img src="~/static/icons/teddy.png" alt="" />
      </div>
      <div class="icon-sidebar flex flex-col">
        <NuxtLink to="/"><button class="btn flex">
            <img src="~/static/icons/dashboard.png" alt="" />Dashboard
          </button>
        </NuxtLink>
        <NuxtLink to="/account">
          <button class="btn flex">
            <img src="~/static/icons/account.png" alt="" />
            Account
          </button>
        </NuxtLink>
        <NuxtLink to="/calculator">
        <button class="btn flex">
          <img src="~/static/icons/calculator.png" alt="" />Calculator
        </button>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.side-bar {
  background: #26201a;
  padding: 0 30px;

  .banner-container {
    margin-top: 50px;
  }

  .icon-sidebar-img {
    img {
      margin: 0 auto;
    }
  }

  .icon-sidebar {
    .btn {
      width: 304px;
      height: 72px;
      align-items: center;
      margin: 20px 5px;

      &:hover {
        background: #ffb039;
        border: 4px solid #fff8f8;
      }
    }
  }
}
</style>