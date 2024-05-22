<script setup lang="ts">
import { reactive } from 'vue';

let state = reactive({
    defaultIdx: 0,
    selectedIdx: 0,
    isCollpase: true,
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
    reloadAction() {
    },
    scrollIntoView(target: string) {
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

function collpaseAction() {
    console.log("collpseAction")
    state.isCollpase = !state.isCollpase
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
                    :class="state.selectedIdx == i ? 'menu-item-selected' : 'menu-item-unselected'"
                    @click="clickAction(item.action, i)">
                    {{ item.title }}</div>

                <div class="collpase-item" @click="collpaseAction">
                    <img src="../assets/icon_nav_menu@2x.png" width="40" height="40" alt="">
                </div>
            </div>
        </el-header>

        <div class="collpase-menu-view" :class="state.isCollpase ? 'hidden-view' : 'show-view'">
            <div v-for="(item, i) in state.menuItems" :key="i" class="wcolor f16 collpase-menu-item"
                :class="state.selectedIdx == i ? 'menu-item-selected' : 'menu-item-unselected'"
                @click="clickAction(item.action, i)">
                {{ item.title }}</div>
        </div>
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



@media screen and (max-width: 767px) {
    .menu-item {
        display: none;
    }

    .collpase-menu-view {
        background: rgba(6, 15, 50);
    }

    .collpase-menu-item {
        width:90%;
        margin: 0 auto;
        height: 48px;
        font-weight: 400;
        font-size: 16px;
        color: #FFFFFF;
        line-height: 48px;
        text-align: center;
        font-style: normal;
        text-transform: none;
    }

    .show-view {
        display: block;
    }

    .hidden-view {
        display: none;
    }
}

@media screen and (min-width: 768px) {
    .menu-item {
        margin-left: 30px;
        margin-right: 30px;
        cursor: pointer;
    }

    .collpase-menu-view {
        display: none;
    }

    .collpase-item {
        display: none;
    }
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