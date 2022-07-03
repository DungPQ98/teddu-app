<template>
    <div class="w-full h-full caculator">
        <div class="caculator-container">
            <div class="flex part-1">
                <Card :title="'TEDDINU Price'" :price="'$14.91'" />
                <div class="mg-card">
                    <Card :title="'Current APY'" :price="'383,025.8%'" />
                </div>
                <Card :title="'Your TEDDINU Balance'" :price="'0 SAFUU'" />
            </div>
            <div class="part-2 flex">
                <div class="left">
                    <Input :label="'TEDDINU Amount'" />
                    <Input :label="'TEDDINU price at purchase ($)'" />
                    <Input :label="'APY (%)'" />
                    <Input :label="'Future TEDDINU market price ($)'" />
                </div>
                <div class="right relative w-full h-full flex flex-col">
                    <div class="background">
                        <img src="~/static/images/bg-caculator.png" alt="">
                    </div>
                    <div class="content">
                        <div class="duration">
                            <div class="day">
                                <span class="text">30 days</span>
                                <span class="text">First Year : 0.02355% Per EPOCH</span>
                            </div>
                            <div class="ratio">
                                <img src="~/static/images/ratio-day.png" alt="">
                            </div>
                        </div>
                        <div class="duration">
                            <div class="year">
                                <span class="text">Second Year : 0.00211% Per EPOCH</span>
                            </div>
                            <div class="ratio">
                                <img src="~/static/images/ratio-year.png" alt="">
                            </div>
                        </div>
                        <div class="infomation">
                            <div v-for="(item, index) of data" :key="index" class="flex line">
                                <div class="title">{{ item.title }}</div>
                                <div class="value" :class="index === 1 ? 'mg-top' : ''">{{ item.value }}</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import Card from '~/components/Dashboard/Card.vue';
import Input from '~/components/Caculator/Input.vue';
export default {
    components: {
        Card,
        Input
    },
    data() {
        return {
            data: [
                {
                    title: 'Your initial investment',
                    value: '$0'
                },
                {
                    title: 'Current wealth',
                    value: '0 TEDDINU'
                },
                {
                    title: 'TEDDINU rewards estimation',
                    value: '$0'
                },
                {
                    title: 'Potential return',
                    value: '$0'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.card {
    max-width: 421px;
}

.mg-card {
    margin: 0 40px;
}

.caculator-container {
    padding-top: 13px;

    .part-1 {
        justify-content: center;
    }

    .part-2 {
        justify-content: center;
        margin-top: 32px;

        .left {
            width: 35%;
            margin-top: 10px;
            padding: 0 30px;
        }

        .right {
            width: 65%;
            font-weight: 400;
            font-size: 24px;
            color: #000000;

            .background {
                position: absolute;
                z-index: 1;
            }

            .duration {
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                padding-top: 36px;
            }

            .content {
                z-index: 2;
            }

            .day {
                width: 86%;
                display: flex;
                justify-content: space-around;
            }

            .year {
                width: 74%;
            }

            .infomation {
                padding-top: 30px;

                .line {
                    width: 85%;
                    align-items: center;
                    margin: 0 auto;
                    border-bottom: 2px solid #000000;
                    padding: 10px;

                    .title {
                        width: 80%;
                    }

                    .value {
                        width: 20%;
                    }
                }
            }
        }
    }
}
</style>