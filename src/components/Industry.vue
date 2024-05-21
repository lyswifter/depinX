<script setup lang="ts">
</script>

<template>
    <div style="background: rgba(9, 20, 58);">
        <div class="industry-view">
            <div class="mid-view-2">
                <div class="id-title-view">Industry Background</div>
                <br>
                <div class="line-2"></div>
                <br>
                <div class="text-3">
                    DePIN stands for "Decentralized Physical Infrastructure Networks," representing a new type
                    of decentralized network for physical infrastructure. The goal of this network is to
                    integrate
                    and activate scattered physical resources, such as hard drives and computational power, to
                    create a vast infrastructure network.
                </div>
                <br>
                <div class="text-3">
                    DePIN projects are numerous, with over 100 initiatives contributing to a market value
                    exceeding $10 billion. These projects are expected to see significant growth, with
                    potential to expand to a scale of $100 billion to $200 billion within 1-2 years.
                </div>
                <div class="text-4">
                    According to projections by Messari, by the year 2028, the DePIN sector could grow to a
                    staggering $3.5 trillion, providing ample growth space and strategic direction for our fund.
                </div>

                <div class="industry-change-view">
                    <div class="s-1">
                        <div class="card-t-1">DePIN Projects</div>
                        <br>
                        <div class="card-t-2">100+</div>
                        <img src="../assets/industry_depin_projects@2x.png" width="286" height="299" alt="">
                    </div>
                    <div class="s-2">
                        <div class="card-t-1">Projected Growth by 2028</div>
                        <br>
                        <div class="card-t-2">Expected to reach $3.5 trillion</div>
                        <img src="../assets/industry_projected_growth@2x.png" width="286" height="400" alt="">
                    </div>
                    <div class="s-3">
                        <div class="card-t-1">DePIN Market Value</div>
                        <br>
                        <div class="card-t-2">Over $10 billion</div>
                        <img src="../assets/industry_market_value@2x.png" width="286" height="461" alt="">
                    </div>
                    <div class="s-4">
                        <div class="card-t-1">Growth Potential in 1-2 Years</div>
                        <br>
                        <div class="card-t-2">$1 trillion to $2 trillion</div>
                        <img src="../assets/industry_growth_potential@2x.png" width="286" height="537" alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.industry-view {
    width: 100%;
    height: 1266px;
    background: linear-gradient(180deg, #07195C 0%, #040C27 100%);
    border-radius: 100px 100px 0px 0px;
}

.mid-view-2 {
    margin: 0 auto;
    width: 1200px;
    padding-top: 140px;
}

.id-title-view {
    width: 703px;
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

.line-2 {
    width: 74px;
    height: 0px;
    border: 2px solid;
    border-image: linear-gradient(90deg, rgba(27, 77, 255, 1), rgba(1, 255, 255, 1)) 2 2;
}

.text-3 {
    width: 1200px;
    height: 75px;
    font-weight: 300;
    font-size: 18px;
    color: #D7E0FF;
    line-height: 25px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.text-4 {
    width: 1200px;
    height: 50px;
    font-weight: 600;
    font-size: 18px;
    color: #D7E0FF;
    line-height: 25px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.industry-change-view {
    display: flex;
}

.s-1 {
    width: 286px;
    height: 414px;
    padding-top: 238px;
}

.s-2 {
    width: 286px;
    height: 642px;
    margin-left: 20px;
    padding-top: 137px
}

.s-3 {
    width: 286px;
    height: 685px;
    margin-left: 20px;
    padding-top: 76px;
}

.s-4 {
    width: 286px;
    height: 838px;
    margin-left: 20px;
}

.card-t-1 {
    width: 226px;
    height: 22px;
    font-weight: 400;
    font-size: 18px;
    color: #FFFFFF;
    line-height: 25px;
    text-align: left;
    font-style: normal;
    text-transform: none;
}

.card-t-2 {
    width: 226px;
    height: 50px;
    font-weight: 600;
    font-size: 36px;
    line-height: 50px;
    text-align: left;
    font-style: normal;
    text-transform: none;
    background-image: linear-gradient(0deg, #1B4DFF 0%, #01FFFF 100%);
    color: transparent;
    background-clip: text;
}
</style>