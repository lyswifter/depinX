<script setup lang="ts">
import { reactive } from 'vue';
import ae from "../assets/portfolio_logo_aethir@2x.png";
import aleo from "../assets/portfolio_logo_aleo@2x.png";
import ar from "../assets/portfolio_logo_arweave@2x.png";
import cel from "../assets/portfolio_logo_celestia@2x.png";
import chia from "../assets/portfolio_logo_chia@2x.png";
import dlink from "../assets/portfolio_logo_deeplink@2x.png";
import icp from "../assets/portfolio_logo_dfinity@2x.png";
import fil from "../assets/portfolio_logo_filecoin@2x.png";
import heli from "../assets/portfolio_logo_helium@2x.png";
import iot from "../assets/portfolio_logo_iotex@2x.png";
import nervos from "../assets/portfolio_logo_nervos@2x.png";
import pol from "../assets/portfolio_logo_polkadot@2x.png";
import polygon from "../assets/portfolio_logo_polygon@2x.png";
import sol from "../assets/portfolio_logo_solana@2x.png";
import uni from "../assets/portfolio_logo_uniswap@2x.png";

let state = reactive({
    portfolios: [[{
        name: "fil",
        logo: fil,
    }, {
        name: "icp",
        logo: icp
    }, {
        name: "chia",
        logo: chia
    }, {
        name: "sol",
        logo: sol
    }, {
        name: "cel",
        logo: cel
    }], [{
        name: "pol",
        logo: pol
    }, {
        name: "ar",
        logo: ar
    }, {
        name: "heli",
        logo: heli
    }, {
        name: "ae",
        logo: ae
    }, {
        name: "dlink",
        logo: dlink
    }], [{
        name: "uni",
        logo: uni,
    }, {
        name: "aleo",
        logo: aleo,
    }, {
        name: "nervos",
        logo: nervos,
    }, {
        name: "iot",
        logo: iot,
    }, {
        name: "polygon",
        logo: polygon,
    }]]
})

// script.js
document.addEventListener('DOMContentLoaded', () => {
    const boxes = document.querySelectorAll('.logo-v');

    const checkBoxes = () => {
        const triggerBottom = window.innerHeight * 0.9;

        boxes.forEach(box => {
            const boxTop = box.getBoundingClientRect().top;

            if (boxTop < triggerBottom) {
                box.classList.add('show');
            } else {
                box.classList.remove('show');
            }
        });
    };

    window.addEventListener('scroll', checkBoxes);

    // Initial check to see if any boxes are already in view
    checkBoxes();
});
</script>

<template>
    <div class="portfolio-view">
        <div class="title-v">
            <div class="mid-view">
                <div class="title title-f">Our Portfolio</div>
            </div>
        </div>

        <div class="content-v">
            <div class="mid-view">
                <div class="logo-view">
                    <div v-for="(itemOut, i) in state.portfolios" :key="i" class="row-view">
                        <div v-for="(itemIn, j) in itemOut" :key="j">
                            <img :src="itemIn.logo" :alt="itemIn.name" class="logo-v logo-v-trans">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.portfolio-view {
    background: #011325;
    padding-top: 100px;
}

@media screen and (max-width: 767px) {
    .mid-view {
        width: 90%;
        margin: 0 auto;
    }

    .title-f {
        font-size: 40px;
        line-height: 47px;
    }

    .content-v {
        width: 100%;
        padding-top: 20px;
        padding-bottom: 100px;
        background: no-repeat center/100% url(../assets/portfolio_bg@2x.png);
        background-size: cover;
    }

    .logo-v {
        height: 52px;
        margin-left: 5px;
        padding: 6px 10px;
        background: rgba(6, 15, 50, 0.54);
        border-radius: 10px 10px 10px 10px;
        border: 1px solid rgba(63, 102, 242, 0.39);
    }
}

@media screen and (min-width: 768px) {
    .mid-view {
        width: 1200px;
        margin: 0 auto;
    }


    .title-f {
        font-size: 64px;
        line-height: 75px;
    }

    .content-v {
        width: 100%;
        padding-bottom: 200px;
        background: no-repeat center/100% url(../assets/portfolio_bg@2x.png);
        background-size: cover;
    }

    .logo-v {
        height: 52px;
        margin-left: 10px;
        margin-top: 20px;
        padding: 20px 30px;
        background: rgba(6, 15, 50, 0.54);
        border-radius: 10px 10px 10px 10px;
        border: 1px solid rgba(63, 102, 242, 0.39);
    }
}

.title-v {
    width: 100%;
    background: #040C27;
}

.title {
    font-weight: 600;
    text-align: left;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(179.9999385867923deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}

.row-view {
    display: flex;
    flex-wrap: wrap;
    justify-content: start;
}

.logo-v:hover {
    border-color: rgba(27, 77, 255, 1);
}

.logo-v-trans {
    opacity: 0;
    transform: scale(0);
    transition: transform 1s ease-in, opacity 1s ease-in;
}

.logo-v.show {
    opacity: 1;
    transform: scale(1);;
}
</style>