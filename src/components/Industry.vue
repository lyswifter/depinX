<script setup lang="ts">
import { reactive } from 'vue';

let state = reactive({
    items: [{
        title: "DePIN Projects",
        content: "100+",
        img: 'one',
        size: 'ssize-1',
    }, {
        title: "Projected Growth by 2028",
        content: "Expected to reach $3.5 trillion",
        img: 'two',
        size: 'ssize-2',
    }, {
        title: "DePIN Market Value",
        content: "Over $10 billion",
        img: 'three',
        size: 'ssize-3',
    }, {
        title: "Growth Potential in 1-2 Years",
        content: "$1 trillion to $2 trillion",
        img: 'four',
        size: 'ssize-4',
    }]
})
</script>

<template>
    <div style="background: rgba(9, 20, 58);">
        <div class="industry-view">
            <div class="mid-view-2">
                <div class="id-title-view id-title-font">Industry Background</div>
                <br>
                <div class="line-2"></div>
                <br>
                <div class="text-3 text-3-f">
                    DePIN stands for "Decentralized Physical Infrastructure Networks," representing a new type
                    of decentralized network for physical infrastructure. The goal of this network is to
                    integrate
                    and activate scattered physical resources, such as hard drives and computational power, to
                    create a vast infrastructure network.
                </div>
                <br>
                <div class="text-3 text-3-f">
                    DePIN projects are numerous, with over 100 initiatives contributing to a market value
                    exceeding $10 billion. These projects are expected to see significant growth, with
                    potential to expand to a scale of $100 billion to $200 billion within 1-2 years.
                </div>
                <br>
                <div class="text-4 text-3-f">
                    According to projections by Messari, by the year 2028, the DePIN sector could grow to a
                    staggering $3.5 trillion, providing ample growth space and strategic direction for our fund.
                </div>

                <div class="industry-change-view">
                    <div class="industry-content-view">
                        <div v-for="(item, i) in state.items" :key="i" class="s-card" :class="[item.img, item.size]">
                            <div class="content-view">
                                <div class="card-t1 card-t1-f">{{ item.title }}</div>
                                <div class="card-t2 card-t2-f">{{ item.content }}</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.industry-view {
    width: 100%;
    background: linear-gradient(180deg, #07195C 0%, #040C27 100%);
    border-radius: 100px 100px 0px 0px;
}

.id-title-view {
    font-weight: 600;
    text-align: left;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(179deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}

@media screen and (max-width: 767px) {
    .mid-view-2 {
        margin: 0 auto;
        width: 78%;
        padding-top: 70px;
    }

    .id-title-font {
        font-size: 40px;
        line-height: 47px;
    }

    .text-3-f {
        font-size: 14px;
        line-height: 20px;
    }
}

@media screen and (min-width: 768px) {
    .mid-view-2 {
        margin: 0 auto;
        width: 62.5%;
        padding-top: 140px;
    }

    .id-title-font {
        font-size: 64px;
        line-height: 75px;
    }

    .text-3-f {
        font-size: 18px;
        line-height: 25px;
    }
}

.line-2 {
    width: 74px;
    height: 0px;
    border: 2px solid;
    border-image: linear-gradient(90deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 2 2;
}

.text-3 {
    font-weight: 300;
    color: #D7E0FF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.text-4 {
    font-weight: 600;
    color: #D7E0FF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.industry-content-view {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    flex-direction: row;
}

@media screen and (max-width: 767px) {
    .ssize-1 {
        width: 138px;
        height: 231px;
    }

    .ssize-2 {
        width: 138px;
        height: 231px;
    }

    .ssize-3 {
        width: 138px;
        height: 231px;
    }

    .ssize-4 {
        width: 138px;
        height: 231px;
    }
}

@media screen and (min-width: 768px) {
    .ssize-1 {
        width: 286px;
        height: 299px;
    }

    .ssize-2 {
        width: 286px;
        height: 400px;
    }

    .ssize-3 {
        width: 286px;
        height: 463px;
    }

    .ssize-4 {
        width: 286px;
        height: 537px;
    }
}

.s-card {
    align-self: end;
    border: 1px solid rgba(63, 102, 242, 0.39);
    border-radius: 10px;
    margin-top: 30px;
}

.one {
    background: no-repeat center/100% url(../assets/industry_depin_projects@2x.png);
    background-position: bottom;
}

.two {
    background: no-repeat center/100% url(../assets/industry_projected_growth@2x.png);
    background-position: bottom;
}

.three {
    background: no-repeat center/100% url(../assets/industry_market_value@2x.png);
    background-position: bottom;
}

.four {
    background: no-repeat center/100% url(../assets/industry_growth_potential@2x.png);
    background-position: bottom;
}

.card-t1 {
    font-weight: 400;
    color: #FFFFFF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.card-t2 {
    font-weight: 600;
    text-align: left;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(0deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}

@media screen and (max-width: 767px) {
    .content-view {
        margin-left: 20px;
        margin-right: 20px;
        margin-top: 30px;
    }

    .card-t1-f {
        font-size: 13px;
        line-height: 18px;
    }

    .card-t2-f {
        font-size: 16px;
        line-height: 22px;
    }
}

@media screen and (min-width: 768px) {
    .content-view {
        margin-left: 30px;
        margin-right: 30px;
        margin-top: 30px;
    }

    .card-t1-f {
        font-size: 18px;
        line-height: 25px;
    }

    .card-t2-f {
        font-size: 36px;
        line-height: 50px;
    }
}
</style>