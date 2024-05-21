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
</script>

<template>
    <div class="container">
        <el-container>

            <!-- header view -->
            <HeaderView></HeaderView>

            <el-main class="main-view">

                <!-- video container view -->
                <VideoView></VideoView>

                <!-- industry background container view -->
                <IndustryView></IndustryView>

                <!-- we provide container view -->
                <ServiceView></ServiceView>

                <!-- Why container view -->
                <WhyView></WhyView>

                <!-- Portfolio container view -->
                <PortfolioView></PortfolioView>

                <!-- Touch container view -->
                <TouchView></TouchView>

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
    /* background: #040C27; */
}

.footer-view {
    padding: 0;
}
</style>
