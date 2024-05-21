<script setup lang="ts">
import FooterView from "./Footer.vue";
import HeaderView from "./Header.vue";
import IndustryView from "./Industry.vue";
import PortfolioView from "./Portfolio.vue";
import ServiceView from "./Service.vue";
import TouchView from "./Touch.vue";
import VideoView from "./Video.vue";
import WhyView from "./Why.vue";

defineProps<{ msg: string }>()

function reloadAction() {
    location.reload();
}

function scrollIntoView(aim: string) {
    document.getElementById(aim)?.scrollIntoView({
        behavior: "smooth",
    });
}

function toTopAction() {
    document.getElementById('topRowAnchor')?.scrollIntoView({
        behavior: "smooth",
    });
}

function scrollToNextView(target: string) {
    document.getElementById(target)?.scrollIntoView({
        behavior: "smooth",
    });
}
</script>

<template>
    <div class="container">
        <el-container>
            <div id="topRowAnchor"></div>
            <!-- header view -->
            <HeaderView @reload-action="reloadAction" @scroll-into-view="scrollIntoView"></HeaderView>

            <div class="to-top-view" @click="toTopAction">
                <div class="to-top-title">Back To Top</div><img src="../assets/arrow_up_nor@2x.png" width="16"
                    height="16" style="margin-top: 15px;margin-left: 2px;" alt="">
            </div>

            <el-main class="main-view">

                <!-- video container view -->
                <VideoView id="AboutAnchor" @scrollToNextView="scrollToNextView"></VideoView>

                <!-- industry background container view -->
                <IndustryView id="IndustryAnchor"></IndustryView>

                <!-- we provide container view -->
                <ServiceView id="ContentAnchor"></ServiceView>

                <!-- Why container view -->
                <WhyView id="CheckerNodeAnchor"></WhyView>

                <!-- Portfolio container view -->
                <PortfolioView id="PortfolioAnchor"></PortfolioView>

                <!-- Touch container view -->
                <TouchView id="ContactAnchor"></TouchView>

            </el-main>

            <el-footer class="footer-view">
                <FooterView></FooterView>
            </el-footer>
        </el-container>
    </div>
</template>

<style scoped>
.main-view {
    padding: 0;
}

.footer-view {
    padding: 0;
}

.to-top-view {
    display: flex;
    position: fixed;
    right: 50px;
    bottom: 180px;
    width: 124px;
    height: 44px;
    background: rgba(215, 224, 255, 0.1);
    border-radius: 4px 4px 4px 4px;
    cursor: pointer;
}

.to-top-title {
    width: 84px;
    height: 17px;
    margin-left: 8px;
    font-weight: 400;
    font-size: 14px;
    color: #D7E0FF;
    line-height: 48px;
    text-align: right;
    font-style: normal;
    text-transform: none;
}
</style>
