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

function leaveAction(index: number) {
    console.log(index)
    state.services[index].isHover = false
}

function rightClick() {
    document.getElementsByClassName('service-list')[0].scrollBy({
        left: 100,
        behavior: 'smooth',
    })
}

function leftClick() {
    document.getElementsByClassName('service-list')[0].scrollBy({
        left: -100,
        behavior: 'smooth',
    })
}
</script>

<template>
    <!-- :onmouseenter="enterAction" :onmouseout="outAction" -->
    <!-- :onmouseover="hoverAction(i)" -->
    <div>
        <div class="service-view">
            <div class="mid-view">
                <div class="service-title">What We Can Provide</div>
                <div class="service-list">
                    <div v-for="(item, i) in state.services" :key="i" class="service-card" @mouseover="hoverAction(i)"
                        @mouseleave="leaveAction(i)">
                        <div class="normal-card" v-if="!item.isHover">
                            <div class="normal-content">
                                <img :src="item.img" width="320" height="382" alt="">
                            </div>
                            <div class="normal-title">{{ item.title }}</div>
                        </div>
                        <div class="hover-card" v-else>
                            <br>
                            <div class="hover-title">{{ item.title }}</div>
                            <br>
                            <div class="hover-content">{{ item.hoverContent }}</div>
                        </div>
                    </div>
                </div>

                <div style="display: flex;margin-top: 60px;margin-left: 40px;">
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
    padding-bottom: 100px;
    background: #040C27;
}

.mid-view {
    margin: 0 auto;
    width: 1200px;
}

.service-title {
    width: 726px;
    height: 78px;
    font-weight: 600;
    font-size: 64px;
    line-height: 75px;
    text-align: left;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(179deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}

.service-list {
    width: 100%;
    margin-top: 80px;
    display: flex;
    overflow-x: scroll;
}

.service-card {
    margin-left: 40px;
    width: 400px;
    background: linear-gradient(180deg, #0B1841 0%, #050E2D 100%);
    border-image: linear-gradient(90deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 4 4;
    border-bottom: 4px solid;
    border-radius: 30px;
    clip-path: inset(0 round 10px);
}

.service-card:hover {
    border-bottom: none;
}

.normal-card {
    width: 400px;
    height: 580px;
}

.normal-title {
    width: 100%;
    font-weight: 600;
    font-size: 32px;
    color: #FFFFFF;
    line-height: 38px;
    text-align: center;
    font-style: normal;
    text-transform: none;
}

.hover-card {
    width: 400px;
    height: 580px;
    background: linear-gradient(180deg, #1142F0 0%, #15E6E6 100%);
    border-radius: 30px 30px 30px 30px;
}

.hover-title {
    width: 340px;
    margin-left: 40px;
    margin-right: 40px;
    font-weight: 600;
    font-size: 32px;
    color: #FFFFFF;
    line-height: 38px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.hover-content {
    width: 320px;
    height: 350px;
    margin-left: 40px;
    margin-right: 40px;
    font-weight: 400;
    font-size: 18px;
    color: #FFFFFF;
    line-height: 25px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}
</style>