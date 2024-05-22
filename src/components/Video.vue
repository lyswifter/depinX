<script setup lang="ts">
import { defineEmits } from "vue";

const emit = defineEmits({
    scrollToNextView(target: string) {
        console.log(target)
    }
})

function scrollToNextView(target: string) {
    emit('scrollToNextView', target)
}
</script>

<template>
    <div>
        <div class="video-container video-height">
            <video class="myvideo" src="../assets/shadergradient.webm" muted autoplay="true" loop="true">
            </video>

            <div class="videocontent">
                <div>
                    <img src="../assets/logo_banner@2x.png" width="130" height="97" alt="">
                </div>
                <br>
                <div>
                    <img class="banner-view" src="../assets/txt_banner@2x.png" width="1146px" height="168px" alt="">
                    <img class="banner-m-view" src="../assetsm/txt_banner_for_mobile@2x.png" width="295" height="166"
                        alt="">
                </div>

                <div class="text-1">
                    Connect Physical World With Blockchain
                </div>

                <br>
                <div style="cursor: pointer;" @click="scrollToNextView('VisionAnchor')">
                    <img src="../assets/arrow_down_nor@2x.png" width="40" height="80" alt="">
                </div>
            </div>
        </div>

        <!-- vision container view -->

        <div class="vision-container" id="VisionAnchor">
            <div class="mid-view">
                <div class="line-1">
                </div>
                <br>
                <div class="text-2 text-adopt">
                    Our vision is to support early-stage DePIN projects through various means
                    including technical support (algorithm optimization, hardware and software
                    enhancements, technical maintenance, equipment supply), direct investment,
                    media empowerment, ecosystem incubation, scientist activities, and organizing Hackathon
                    events.
                    We are backed by top Filecoin mining service providers with
                    an asset management scale of $20 million.
                </div>
                <br>
                <div class="text-2 text-adopt">
                    Our core members boast over five
                    years of IT and blockchain industry experience at leading institutions such as
                    Google, Baidu, Hashkey, and OKX, and are globally distributed in Hong Kong,
                    Singapore, Australia, and North America.
                </div>
            </div>

        </div>
        <div class="ball-dot-view">
            <img src="../assets/ball_dot@2x.png" alt="">
        </div>
    </div>
</template>

<style scoped>
.video-container {
    position: relative;
    width: 100%;
    overflow: hidden;
}

.myvideo {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: -2;
}

.videocontent {
    position: absolute;
    top: 90px;
    left: 10%;
    width: 100%;
    color: white;
}

.vision-container {
    width: 100%;
    padding-bottom: 200px;
    background: rgba(9, 20, 58);
}

.line-1 {
    width: 0px;
    height: 80px;
    border-radius: 0px 0px 0px 0px;
    border: 2px solid;
    border-image: linear-gradient(360deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 2 2;
}

.text-2 {
    width: 100%;
    max-width: 820px;
    font-weight: 400;
    color: #D7E0FF;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

@media screen and (max-width: 767px) {
    .mid-view {
        margin: 0 auto;
        width: 78%;
        padding-top: 80px;
    }

    .ball-dot-view {
        display: none;
    }

    .banner-view {
        display: none;
    }

    .text-1 {
        width: 295px;
        height: 58px;
        font-weight: 300;
        font-size: 24px;
        color: #D7E0FF;
        line-height: 28px;
        text-align: left;
        font-style: normal;
        text-transform: none;
    }

    .text-adopt {
        font-size: 16px;
        line-height: 26px;
    }

    .video-height {
        height: 600px;
    }
}

@media screen and (min-width: 768px) {
    .mid-view {
        margin: 0 auto;
        width: 62.5%;
        padding-top: 80px;
    }

    .ball-dot-view img {
        position: absolute;
        right: 0;
        top: 80%;
        bottom: 50%;
        width: 550px;
        height: 1100px;
        z-index: 1;
    }

    .banner-m-view {
        display: none;
    }

    .text-1 {
        max-width: 807px;
        height: 49px;
        font-weight: 300;
        font-size: 40px;
        color: #D7E0FF;
        line-height: 47px;
        text-align: left;
        font-style: normal;
        text-transform: none;
    }

    .text-adopt {
        font-size: 28px;
        line-height: 45px;
    }

    .video-height {
        height: 900px;
    }
}
</style>