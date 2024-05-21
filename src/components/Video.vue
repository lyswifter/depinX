<script setup lang="ts">
import { defineEmits } from "vue";

const emit = defineEmits({
    scrollToNextView(target: string){}
})

function scrollToNextView(target: string) {
    emit('scrollToNextView', target)
}
</script>

<template>
    <div>
        <div class="video-container">
            <video class="myvideo" src="../assets/shadergradient.webm" muted autoplay="true" loop="true">
            </video>

            <div class="videocontent">
                <div>
                    <img src="../assets/logo_banner@2x.png" width="130" height="97" alt="">
                </div>

                <div>
                    <img src="../assets/txt_banner@2x.png" width="1146px" height="168px" alt="">
                </div>

                <div class="text_1">
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
                <div class="line_1">

                </div>
                <div class="text_2">
                    Our vision is to support early-stage DePIN projects through various means
                    including technical support (algorithm optimization, hardware and software
                    enhancements, technical maintenance, equipment supply), direct investment,
                    media empowerment, ecosystem incubation, scientist activities, and organizing Hackathon
                    events.
                    We are backed by top Filecoin mining service providers with
                    an asset management scale of $20 million.
                </div>

                <br>

                <div class="text_2">
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
    height: 908px;
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
    top: 30%;
    left: 10%;
    width: 1200px;
    color: white;
}

.text_1 {
    width: 807px;
    height: 49px;
    font-weight: 300;
    font-size: 40px;
    color: #D7E0FF;
    line-height: 47px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.vision-container {
    width: 100%;
    padding-bottom: 200px;
    background: rgba(9, 20, 58);
}

.mid-view {
    margin: 0 auto;
    width: 1200px;
    padding-top: 200px;
}

.line_1 {
    width: 0px;
    height: 80px;
    border-radius: 0px 0px 0px 0px;
    border: 2px solid;
    border-image: linear-gradient(360deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 2 2;
}

.text_2 {
    width: 820px;
    font-weight: 400;
    font-size: 28px;
    color: #D7E0FF;
    line-height: 45px;
    text-align: left;
    font-style: normal;
    text-transform: none;
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
</style>