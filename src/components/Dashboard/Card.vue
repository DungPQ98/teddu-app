<template>
    <div class="card">
        <div class="inner-card">
            <div class="title">
                {{ title }}
            </div>
            <div class="price">
                {{ price }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: String,
        price: String
    }
}
</script>

<style lang="scss" scoped>
.card {
    max-width: 400px;
    border: 4px solid #000000;
    filter: drop-shadow(0px 24px 12px rgba(0, 0, 0, 0.1));

    .partern {
        margin: 0 17px;
    }

    .inner-card {
        padding: 10px 0 0 0;
        margin: 8px 4px;
        background: linear-gradient(0deg, #EFE9E0 -38.96%, #FFFFFF 127.83%);
        border: 8px solid #FFFFFF;
        box-shadow: 0px 24px 12px rgba(0, 0, 0, 0.1);
        font-weight: 400;
        font-size: 32px;
        text-align: center;

        .title {
            color: #000000;
            padding-bottom: 13px;
            min-width: 312px;
        }

        .price {
            width: 100%;
            background: #985C23;
            color: #FFB039;
        }
    }
}
</style>