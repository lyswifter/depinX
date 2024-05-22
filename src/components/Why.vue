<script setup lang="ts">
import { reactive } from 'vue';
import first from '../assets/acnode_best_revenue@2x.png';
import third from '../assets/acnode_clear_output@2x.png';
import fourth from '../assets/acnode_data_center@2x.png';
import second from '../assets/acnode_one_click_mining@2x.png';
import dot from '../assets/icon_acnode_tag@2x.png';

let state = reactive({
    features: [[{
        title: "The best revenue spliton the entire network",
        content: "95 : 5, You take 95%",
        img: first,
        cls: "one",
        dot: dot
    }, {
        title: "One-Click Mining",
        content: "You provide the NFT. I'll handle everything else.",
        img: second,
        cls: "two",
        dot: dot
    }], [{
        title: "Clear and transparentproft sharing",
        content: "Clear and transparent output/revenue. Investors can see it !",
        img: third,
        cls: "three",
        dot: dot
    }, {
        title: "The best revenue spliton the entire network",
        content: "Southeast Asia Tier 3 data center + Our 10 years of blockchain technology maintenancev",
        img: fourth,
        cls: "four",
        dot: dot
    }]]
})
</script>

<template>
    <div>
        <div class="why-view">
            <div class="mid-view">
                <div class="logo-view">
                    <img src="../assets/ac_node@2x.png" width="100%" alt="">
                </div>
                <br>
                <div class="text-1 text-1-f">WHY CHOOSE DePIN X ?</div>
                <br>
                <div class="feature-view">
                    <div v-for="(itemOut, i) in state.features" :key="i" class="row-view">
                        <div v-for="(itemIn, j) in itemOut" :key="j">
                            <div class="item-card card-size">
                                <div style="width: 90%;height: 90%;margin: 0 auto;margin-top: 30px;"
                                    :class="itemIn.cls">
                                    <div><img :src="itemIn.dot" width="31" height="16" alt=""></div>
                                    <div class="title-v title-v-f">{{ itemIn.title }}</div>
                                    <div class="content-v content-v-f">{{ itemIn.content }}</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <br>
                <div class="checknode-view">
                    <div style="margin: 40px;">
                        <div class="text-2 text-2-f">
                            Run a Checker Node!
                        </div>
                        <div class="text-3 text-3-f">
                            —— Your best choice !
                        </div>

                        <div style="display: flex;flex-wrap: wrap;">
                            <div class="contact-v">
                                <div class="text-4">Contact</div>
                                <br>
                                <div style="display: flex;">
                                    <img src="../assets/icon_wechat@2x.png" width="20" height="20" alt="">
                                    <div class="text-5">wxid 5bzocyoxb5hi21</div>
                                </div>
                                <br>
                                <div style="display: flex;">
                                    <img src="../assets/icon_tg@2x.png" width="20" height="20" alt="">
                                    <div class="text-5">@DEPINX OFFICIAL</div>
                                </div>
                            </div>

                            <div class="flex-grow" />

                            <div class="qr-code-v">
                                <div class="qr-code">
                                    <img src="../assets/code_wechat_checker_node@2x.png" width="100%" height="100%"
                                        alt="">
                                </div>
                                <div class="qr-code" style="margin-left: 40px;">
                                    <img src="../assets/code_tg_checker_node@2x.png" width="100%" height="100%" alt="">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.why-view {
    width: 100%;
    padding-top: 80px;
    background: linear-gradient(180deg, #07195C 0%, #040C27 50%);
}

@media screen and (max-width: 767px) {
    .mid-view {
        width: 90%;
        max-width: 1200px;
        margin: 0 auto;
    }

    .logo-view {
        width: 270px;
        margin: 0 auto;
    }

    .text-1-f {
        font-size: 44px;
        line-height: 52px;
    }

    .card-size {
        width: 335px;
        height: 230px;
    }

    .title-v-f {
        font-size: 20px;
        line-height: 23px;
    }

    .content-v-f {
        font-size: 14px;
        line-height: 20px;
    }

    .row-view {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
}

@media screen and (min-width: 768px) {
    .mid-view {
        width: 1200px;
        margin: 0 auto;
    }

    .logo-view {
        width: 540px;
        margin: 0 auto;
    }

    .text-1-f {
        font-size: 94px;
        line-height: 110px;
    }

    .card-size {
        width: 580px;
        height: 350px;
    }

    .title-v-f {
        font-size: 30px;
        line-height: 35px;
    }

    .content-v-f {
        font-size: 18px;
        line-height: 25px;
    }

    .row-view {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
}

.text-1 {
    width: 100%;
    margin: 0 auto;
    font-weight: 200;
    text-align: center;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(179.9999385867923deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}

.feature-view {
    width: 100%;
    margin: 0 auto;
}

.item-card {
    margin-top: 30px;
    border-radius: 30px 30px 30px 30px;
    border: 1px solid rgba(63, 102, 242, 0.3);
}

.item-card:hover {
    border-color: rgba(27, 77, 255, 1);
}

.one {
    background: no-repeat center/100% url(../assets/acnode_best_revenue@2x.png);
}

.two {
    background: no-repeat center/100% url(../assets/acnode_one_click_mining@2x.png);
}

.three {
    background: no-repeat center/100% url(../assets/acnode_clear_output@2x.png);
}

.four {
    background: no-repeat center/100% url(../assets/acnode_data_center@2x.png);
}

.title-v {
    font-weight: 600;
    color: #FFFFFF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.content-v {
    width: 60%;
    font-weight: 400;
    color: #B7C5F6;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

/* ----- */

.checknode-view {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    margin-top: 40px;
    border-radius: 30px;
    border: 1px solid rgba(63, 102, 242, 0.3);
    background: no-repeat center/100% url(../assets/acnode_best_choice@2x.png);
}

.checknode-view:hover {
    border-color: rgba(27, 77, 255, 1);
}

.text-2 {
    font-weight: 600;
    color: #FFFFFF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.text-3 {
    font-weight: 400;
    color: #FFFFFF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.text-4 {
    width: 123px;
    height: 37px;
    font-weight: 600;
    font-size: 30px;
    color: #FFFFFF;
    line-height: 35px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.text-5 {
    margin-left: 5px;
    height: 22px;
    font-weight: 400;
    font-size: 18px;
    color: #D7E0FF;
    line-height: 21px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.contact-v {
    padding-top: 40px;
    margin-top: 80px;
    border-top: 1px solid;
    border-image: linear-gradient(90deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 1 1;
}

.flex-grow {
    flex-grow: 1;
}

.qr-code-v {
    display: flex;
    margin-top: 40px;
}

@media screen and (max-width: 767px) {
    .qr-code {
        width: 137px;
        height: 137px;
    }

    .contact-v {
        width: 100%;
        margin-top: 200px;
    }

    .checknode-view {
        background: no-repeat center/100% url(../assets/acnode_best_choice_mobile@2x.png);
        background-position: top
    }

    .text-2-f {
        font-size: 36px;
        line-height: 42px;
    }

    .text-3-f {
        font-size: 20px;
        line-height: 23px;
    }
}

@media screen and (min-width: 768px) {
    .qr-code {
        width: 151px;
        height: 151px;
    }

    .text-2-f {
        font-size: 48px;
        line-height: 56px;
    }

    .text-3-f {
        font-size: 30px;
        line-height: 35px;
    }
}
</style>