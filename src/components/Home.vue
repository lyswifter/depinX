<script setup lang="ts">
import { ref } from 'vue';
import HeaderView from "./Header.vue";
import VideoView from "./Video.vue";
import IndustryView from "./Industry.vue";
import ServiceView from "./Service.vue";
import FooterView from "./Footer.vue";

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
                
            </el-main>

            <el-footer>
                <FooterView></FooterView>
            </el-footer>
        </el-container>
    </div>
</template>

<style scoped>
.main-view {
    padding: 0;
}
</style>
