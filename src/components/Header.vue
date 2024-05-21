<script setup lang="ts">
import { defineEmits, reactive } from 'vue';

let state = reactive({
    defaultIdx: 0,
    selectedIdx: 0,
    menuItems: [{
        index: 0,
        title: "About",
        action: "AboutAnchor",
    }, {
        index: 1,
        title: "Industry Background",
        action: "IndustryAnchor",
    }, {
        index: 2,
        title: "Content",
        action: "ContentAnchor",
    }, {
        index: 3,
        title: "Aethir Checker Node",
        action: "CheckerNodeAnchor",
    }, {
        index: 4,
        title: "Portfolio",
        action: "PortfolioAnchor",
    }, {
        index: 5,
        title: "Contact",
        action: "ContactAnchor",
    }]
})

const emit = defineEmits({
    reloadAction(){
    },
    scrollIntoView(target: string){
        console.log("emit target:" + target)
    },
})

function clickAction(target: string, idx: number) {
    state.selectedIdx = idx
    emit('scrollIntoView', target)
}

function reloadAction() {
    state.selectedIdx = 0
    emit('reloadAction')
}
</script>

<template>
    <div>
        <el-header class="header">
            <div>
                <a href="javascript:void(0)" @click="reloadAction">
                    <img style="width: 154px" src="../assets/logo_nav@2x.png" alt="depinX" />
                </a>
            </div>

            <div class="flex-grow" />

            <div style="display: flex;">
                <div v-for="(item, i) in state.menuItems" :key="i" class="wcolor f16 menu-item" 
                :class="state.selectedIdx == i ? 'menu-item-selected' : 'menu-item-unselected'" @click="clickAction(item.action, i)">
                    {{ item.title }}</div>
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
    cursor: pointer;
}

.menu-item:hover {
  border-bottom: 1px solid white;
}

.menu-item-selected {
    border-bottom: 1px solid white;
}

.menu-item-unselected {
    border-bottom: none;
}

.flex-grow {
    flex-grow: 1;
}

.main-view {
    padding: 0;
}
</style>