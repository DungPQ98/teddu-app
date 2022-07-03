<template>
    <div class="card">
        <div class="inner-card">
            <div class="title">
                {{ title }}
            </div>
            <div class="price">
                {{ price }}
            </div>
            <div class="footer-text">
                {{ footerText }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: String,
        price: String,
        footerText: String
    }
}
</script>

<style lang="scss" scoped>
.card {
    max-width: 400px;

    @media only screen and (min-width: 1900px) {
        max-width: 475px;
    }

    border: 4px solid #000000;
    filter: drop-shadow(0px 24px 12px rgba(0, 0, 0, 0.1));

    .partern {
        margin: 0 17px;
    }

    .inner-card {
        width: 340px;

        @media only screen and (min-width: 1900px) {
            width: 440px;
        }

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
            font-size: 32px;
        }

        .price {
            width: 100%;
            background: #985C23;
            font-size: 48px;
            color: #3DFF39;
        }

        .footer-text {
            color: #000000;
            padding-bottom: 11px;
            padding-top: 8px;
        }
    }
}
</style>