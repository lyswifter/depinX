<script setup lang="ts">
import { reactive } from 'vue';
import one from '../assets/content_capital_liquidity@2x.png';
import four from "../assets/content_consultancy@2x.png";
import two from "../assets/content_hardware@2x.png";
import three from "../assets/content_services@2x.png";

let state = reactive({
    services: [{
        isHover: false,
        img: one,
        title: "Capital/Liquidity",
        hoverContent: "We invest amounts ranging from $200,000 to $1.5 million per transaction, providing ample funds and liquidity to support DePIN projects throughout their development stages, ensuring they receive the necessary boost to thrive.",
    }, {
        isHover: false,
        img: two,
        title: "Hardware Equipment",
        hoverContent: "We possess 20,000 GPUs, 10 sets of H100, and a wealth of other machines and equipment. Currently, we hold mining equipment worth over 300 million USD, which has been running securely for more than 6 years. Our IDC data centers are spread across five cities on three continents, offering extensive hardware resources, blockchain underlying technology development, and operational maintenance technology.",
    }, {
        isHover: false,
        img: three,
        title: "Ecosystem and Media Services",
        hoverContent: "Our fund advisors have successfully designed over 200 token economics models, including for top projects like Filecoin. We offer high-value consultancy advice on token economics models for our investee projects, assisting them in gaining market recognition.",
    }, {
        isHover: false,
        img: four,
        title: "Consultancy Services",
        hoverContent: "We possess the ecosystem operational capabilities required for the future development of DePIN projects, including exclusive public blockchain resources for DePIN, media alliances related to Web3.0, and market credibility enhancement services. These services can further increase the market value of the projects we invest in, thereby realizing an appreciation in fund returns.",
    }]
})

function hoverAction(index: number) {
    console.log(index)
    state.services[index].isHover = true
}

function clickAction(index: number) {
    console.log(index)
    state.services[index].isHover = true
}

function leaveAction(index: number) {
    console.log(index)
    state.services[index].isHover = false
}

function rightClick() {
    document.getElementsByClassName('service-list')[0].scrollBy({
        left: 200,
        behavior: 'smooth',
    })
}

function leftClick() {
    document.getElementsByClassName('service-list')[0].scrollBy({
        left: -200,
        behavior: 'smooth',
    })
}
</script>

<template>
    <div>
        <div class="service-view">
            <div class="mid-view">
                <div class="service-title service-title-f">What We Can Provide</div>

                <div class="service-list">
                    <div v-for="(item, i) in state.services" :key="i" class="service-card"
                        :class="i == 0 ? 'm-l-none' : 'm-l-40'" @mouseover="hoverAction(i)" @mouseleave="leaveAction(i)"
                        @click="clickAction(i)">
                        <div class="normal-card" v-if="!item.isHover">
                            <div class="normal-content">
                                <img :src="item.img" width="100%" height="100%" alt="">
                            </div>
                            <div class="normal-title normal-title-f">{{ item.title }}</div>
                        </div>
                        <div class="hover-card" v-else>
                            <br>
                            <div class="hover-title hover-title-f">{{ item.title }}</div>
                            <div class="hover-content hover-content-f">{{ item.hoverContent }}</div>
                        </div>
                    </div>
                </div>

                <div style="display: flex;margin-top: 60px;">
                    <div style="cursor: pointer;" @click="leftClick">
                        <img src="../assets/arrow_left_nor@2x.png" width="80" height="40" alt="">
                    </div>

                    <div style="margin-left: 20px;cursor: pointer;" @click="rightClick">
                        <img src="../assets//arrow_right_nor@2x.png" width="80" height="40" alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.service-view {
    width: 100%;
    padding-top: 180px;
    padding-bottom: 100px;
    background: #040C27;
}

@media screen and (max-width: 767px) {
    .mid-view {
        margin: 0 auto;
        width: 80%;
    }

    .service-title-f {
        font-size: 40px;
        line-height: 47px;
    }
}

@media screen and (min-width: 768px) {
    .mid-view {
        margin: 0 auto;
        width: 1200px;
    }

    .service-title-f {
        font-size: 64px;
        line-height: 75px;
    }
}

.service-title {
    font-weight: 600;
    text-align: left;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(179deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}

.m-l-40 {
    margin-left: 40px;
}

.m-l-none {
    margin-left: 0px;
}

.service-list {
    width: 100%;
    margin-top: 80px;
    display: flex;
    overflow-x: scroll;
}

.service-card {
    background: linear-gradient(180deg, #0B1841 0%, #050E2D 100%);
    border-image: linear-gradient(90deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 4 4;
    border-bottom: 4px solid;
    border-radius: 30px;
    clip-path: inset(0 round 10px);
}

.service-card:hover {
    border-bottom: none;
}

@media screen and (max-width: 767px) {
    .normal-card {
        width: 240px;
        height: 440px;
    }

    .normal-content {
        width: 200px;
        margin: 0 auto;
    }

    .normal-title-f {
        font-size: 20px;
        line-height: 23px;
    }

    .hover-card {
        width: 240px;
        height: 440px;
        background: linear-gradient(180deg, #1142F0 0%, #15E6E6 100%);
        border-radius: 30px 30px 30px 30px;
    }

    .hover-title-f {
        font-size: 18px;
        line-height: 23px;
    }

    .hover-content-f {
        font-size: 14px;
        line-height: 20px;
    }
}

@media screen and (min-width: 768px) {
    .normal-card {
        width: 400px;
        height: 580px;
    }

    .normal-content {
        width: 320px;
        height: 382px;
        margin: 0 auto;
    }

    .normal-title-f {
        font-size: 32px;
        line-height: 38px;
    }

    .hover-card {
        width: 400px;
        height: 580px;
        background: linear-gradient(180deg, #1142F0 0%, #15E6E6 100%);
        border-radius: 30px 30px 30px 30px;
    }

    .hover-title-f {
        font-size: 32px;
        line-height: 38px;
    }

    .hover-content-f {
        font-size: 18px;
        line-height: 25px;
    }
}

.normal-title {
    font-weight: 600;
    color: #FFFFFF;
    text-align: center;
    font-style: normal;
    text-transform: none;
}

.hover-title {
    width: 85%;
    margin: 0 auto;
    font-weight: 600;
    color: #FFFFFF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.hover-content {
    width: 80%;
    margin: 0 auto;
    font-weight: 400;
    color: #FFFFFF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}
</style>