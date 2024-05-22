<script setup lang="ts">
import { reactive } from "vue";
import arrow from "../assets/arrow_right_up_nor@2x.png";
import icon1 from "../assets/icon@2x_(1).png";
import icon2 from "../assets/icon@2x_(2).png";

let state = reactive({
    links: [{
        logo: icon1,
        title: "@DePIN_X",
        arrow: arrow,
        href: "https://x.com/depin_x",
    }, {
        logo: icon2,
        title: "@DePIN_X",
        arrow: arrow,
        href: "https://www.linkedin.com/company/depin-x-cappital",
    }],
    sites: [{
    }]
})
</script>

<template>
    <div class="touch-view">
        <div class="mid-view">
            <div class="title-v">Get in touch</div>
            <br>
            <div class="content-v border-1">
                <div>
                    <div><img src="../assets/icon@2x.png" width="50" height="50" alt="" class="m-l-40 m-t-40"></div>
                    <div>
                        <div style="display: flex;flex-wrap: wrap;" class="border-b-1">
                            <div class="m-l-40 m-t-40 m-b-40">
                                <div class="text-1">For Investment Cooperation: </div>
                                <a href="mailto:sallygu@depinxcapital.com">
                                    <div style="display: flex;">
                                        <div class="text-2">sallygu@depinxcapital.com</div>
                                        <img src="../assets/arrow_right_up_nor@2x.png" width="16" height="16" alt="">
                                    </div>
                                </a>
                            </div>

                            <div class="m-l-40 m-t-40 m-b-40">
                                <div class="text-1">For Mining Cooperation: </div>
                                <a href="mailto:myron_zhu@depinxcapital.com">
                                    <div style="display: flex;">
                                        <div class="text-2">myron_zhu@depinxcapital.com</div>
                                        <img src="../assets/arrow_right_up_nor@2x.png" width="16" height="16" alt="">
                                    </div>
                                </a>
                            </div>
                        </div>

                        <div style="display: flex;justify-content:center;flex-wrap: wrap;">
                            <div v-for="(item, i) in state.links" :key="i" style="width: 50%;">
                                <div style="padding: 40px;" :class="i != 0 ? 'border-l-1' : 'border-l-none'">
                                    <div><img :src="item.logo" width="50" height="50" alt=""></div>
                                    <a :href="item.href" target="_blank">
                                        <div style="display: flex;justify-content: start;">
                                            <div class="text-2">{{ item.title }}</div>
                                            <img :src="item.arrow" width="16" height="16" alt="">
                                        </div>
                                    </a>
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
.touch-view {
    width: 100%;
    padding-top: 80px;
    padding-bottom: 80px;
    background: linear-gradient(180deg, #07195C 0%, #000000 100%);
}

@media screen and (max-width: 767px) {
    .mid-view {
        width: 90%;
        margin: 0 auto;
    }
}

@media screen and (min-width: 768px) {
    .mid-view {
        width: 62.5%;
        max-width: 1200px;
        margin: 0 auto;
    }
}

.title-v {
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

.text-1 {
    width: 520px;
    height: 22px;
    font-weight: 600;
    font-size: 18px;
    line-height: 21px;
    text-align: left;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(0deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}

.text-2 {
    margin-right: 5px;
    height: 22px;
    font-weight: 400;
    font-size: 18px;
    color: #D7E0FF;
    line-height: 21px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.content-v {
    background: #040C27;
}

.border-1 {
    border: 1px solid rgba(63, 102, 242, 0.39);
}

.border-1:hover {
    border-color: rgba(27, 77, 255, 1);
}

.border-b-1 {
    border-bottom: 1px solid rgba(63, 102, 242, 0.39);
}

.border-b-1:hover {
    border-color: rgba(27, 77, 255, 1);
}

.border-l-1 {
    border-left: 1px solid rgba(63, 102, 242, 0.39);
}

.border-l-1:hover {
    border-color: rgba(27, 77, 255, 1);
}

.border-b-none {
    border-left: none
}

.m-t-40 {
    margin-top: 40px;
}

.m-l-40 {
    margin-left: 40px;
}

.m-b-40 {
    margin-bottom: 40px;
}
</style>