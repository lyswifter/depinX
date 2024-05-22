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
                <div style="width: 540px;margin: 0 auto;">
                    <img src="../assets/ac_node@2x.png" width="540" height="100" alt="">
                </div>
                <br>
                <div style="width: 100%;margin: 0 auto;" class="text-1">WHY CHOOSE DePIN X ?</div>
                <br>
                <div class="feature-view">
                    <div v-for="(itemOut, i) in state.features" :key="i" class="row-view">
                        <div v-for="(itemIn, j) in itemOut" :key="j">
                            <div class="item-card">
                                <div style="width: 520px;height: 290px;margin: 0 auto;margin-top: 30px;"
                                    :class="itemIn.cls">
                                    <div><img :src="itemIn.dot" width="31" height="16" alt=""></div>
                                    <br>
                                    <div class="title-v">{{ itemIn.title }}</div>
                                    <br>
                                    <div class="content-v">{{ itemIn.content }}</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <br>
                <div class="checknode-view">
                    <div class="text-2">
                        Run a Checker Node!
                    </div>
                    <div class="text-3">
                        —— Your best choice !
                    </div>

                    <div style="display: flex;margin-top: 80px;">
                        <div class="contact-v">
                            <div class="text-4">Contact</div>
                            <br>
                            <div style="display: flex;">
                                <img src="../assets/icon_wechat@2x.png" width="20" height="20" alt="">
                                <div class="text-5">wxid 5bzocyoxb5hi21</div>
                            </div>
                            <div style="display: flex;">
                                <img src="../assets/icon_tg@2x.png" width="20" height="20" alt="">
                                <div class="text-5">@DEPINX OFFICIAL</div>
                            </div>
                        </div>
                        <div class="flex-grow" />
                        <div><img src="../assets/code_wechat_checker_node@2x.png" width="151" height="151" alt=""></div>
                        <div style="margin-left: 40px;"><img src="../assets/code_tg_checker_node@2x.png" width="151"
                                height="151" alt=""></div>
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
    /* padding-bottom: 100px; */
    background: linear-gradient(180deg, #07195C 0%, #040C27 50%);
}

.mid-view {
    width: 1200px;
    margin: 0 auto;
}

.text-1 {
    height: 115px;
    font-weight: 200;
    font-size: 94px;
    line-height: 110px;
    text-align: center;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(179.9999385867923deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}

.feature-view {
    width: 1200px;
    margin: 0 auto;
}

.row-view {
    display: flex;
    justify-content: space-between
}

.item-card {
    margin-top: 30px;
    width: 580px;
    height: 350px;
    border-radius: 30px 30px 30px 30px;
    border: 1px solid rgba(63, 102, 242, 0.3);
}

.item-card:hover {
    /* border-radius: 30px 30px 30px 30px;
    background: rgba(6, 15, 50, 0.54);
    border: 1px solid transparent;
    background-clip: padding-box;
    border-image: linear-gradient(90deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 2 2; */
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
    width: 450px;
    height: 74px;
    font-weight: 600;
    font-size: 30px;
    color: #FFFFFF;
    line-height: 35px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.content-v {
    width: 202px;
    font-weight: 400;
    font-size: 18px;
    color: #B7C5F6;
    line-height: 25px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.checknode-view {
    width: 1200px;
    margin: 0 auto;
    margin-top: 40px;
    height: 437px;
    background: no-repeat center/100% url(../assets/acnode_best_choice@2x.png);
}

.text-2 {
    width: 1120px;
    height: 59px;
    font-weight: 600;
    font-size: 48px;
    color: #FFFFFF;
    line-height: 56px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.text-3 {
    width: 1120px;
    height: 37px;
    font-weight: 400;
    font-size: 30px;
    color: #FFFFFF;
    line-height: 35px;
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
    width: 521px;
    padding-top: 40px;
    border-top: 1px solid;
    border-image: linear-gradient(90deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 1 1;
}

.flex-grow {
    flex-grow: 1;
}
</style>