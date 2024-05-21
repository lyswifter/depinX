<script setup lang="ts">
import { ref } from 'vue';

const activeIndex = ref('1')
const handleSelect = (key: string, keyPath: string[]) => {
    console.log(key, keyPath)
}
</script>

<template>
    <div>
        <el-header class="header">
            <div>
                <img style="width: 154px" src="../assets/logo_nav@2x.png" alt="depinX" />
            </div>

            <div class="flex-grow" />

            <div style="display: flex;">
                <div class="wcolor f16 menu-item">About</div>
                <div class="wcolor f16 menu-item">Industry Background</div>
                <div class="wcolor f16 menu-item">Content</div>
                <div class="wcolor f16 menu-item">Aethir Checker Node</div>
                <div class="wcolor f16 menu-item">Portfolio</div>
                <div class="wcolor f16 menu-item">Contact</div>
            </div>
        </el-header>
    </div>
</template>

<style scoped>
.header {
    width: 100%;
    padding-top: 15px;
    background: rgba(6, 15, 50);
    display: flex;
}

.menu-view {
    background: rgba(6, 15, 50);
}

.menu-item {
    margin-left: 30px;
    margin-right: 30px;
}

.flex-grow {
    flex-grow: 1;
}

.main-view {
    padding: 0;
}
</style>