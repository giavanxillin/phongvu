<template>
        <div class="carousel">
        <el-carousel height="550px" :interval="5000" arrow="always">
            <el-carousel-item v-for="c in carousel" :key="c.id">
            <img :src="c.src" alt="">
            </el-carousel-item>
        </el-carousel>
        <div>manh</div>
        <div class="lazyload">
            <el-row>
                <el-col :span="6">
                    <div class="lazyload-image">
                        <img src="../assets/lazyload1.webp" alt="">
                    </div>
                </el-col>
                <el-col :span="6">
                    <div class="lazyload-image">
                        <img src="../assets/lazyload2.webp" alt="">
                    </div>
                </el-col>
                <el-col :span="6">
                    <div class="lazyload-image">
                        <img src="../assets/lazyload3.webp" alt="">
                    </div>
                </el-col>
                <el-col :span="6">
                    <div class="lazyload-image">
                        <img src="../assets/lazyload4.webp" alt="">
                    </div>
                </el-col>
            </el-row>
        </div>
    </div>    
</template>

<script>
export default {
    data() {
        return {
            carousel: [
                {
                    id: 1,
                    src: "https://lh3.googleusercontent.com/bph66C8isd6pj3XbmvmNd4h4pPa4zznWRyvdSog-jqWu1mgA77b9PIQdAuiQCeq4WOyTh4eew0skldig7Q=w1920-rw"
                },
                {
                    id: 2,
                    src: "https://lh3.googleusercontent.com/ViIt-UoHci-PVrza2nm-zAehrhccOLmNRTMPunni14aDFYP9QdH5ZpKZQFP5VpOD9ENWoN1l53f_Jv2altU=w1920-rw"
                },
                {
                    id: 3,
                    src: "https://lh3.googleusercontent.com/rDnSNoA_4GKyWqbG9DGYstKSXeND6iyijxxCAU8q7RUvPmwN6Hs5nTQYzE-rKFgSGfPqU0QlVJZBdk2x91Lx=w1920-rw"
                },
                {
                    id: 4,
                    src: "https://lh3.googleusercontent.com/aYt0Vo3ZkgXph_zUANNyLNadkGgLNufiTcWw99vlt5zcEZzQDf2nXdIQzhEHPWTALDzSmT2CfZ846JsljXfkhJcHTyViNe_pfw=w1920-rw"
                },
                {
                    id: 5,
                    src: "https://lh3.googleusercontent.com/9yu0zIdthK5EuKmZiyIFLASBeaO7k0SGftml9YejIaxeJU16aGVqhIhCySh0zYtvTtqHI40pbbkj99xyNw=w1920-rw"
                },
                {
                    id: 6,
                    src: "https://lh3.googleusercontent.com/KbSfTHG6_YNnXS2GukCw86kTX11dN-ebiro6UkmAyjzHdRq9PBpu0-6vqm6iW9gsXXsbikLmsFYGd1N2VA=w1920-rw"
                },
                {
                    id: 7,
                    src: "https://lh3.googleusercontent.com/lSKfY_KSvHR26MLj9N8LHYZo_5HkEIxn2EXGmQ6fH6GeXVOOet6Q0xun3r2dYlu-IxRn7G7WNe4IMWmR5g=w1920-rw"
                },
                {
                    id: 8,
                    src: "https://lh3.googleusercontent.com/yZVIkXRz0yMEEMbZxkmunz1Nf4eTBhwGLe7CfLdSurmlFNysAKg7DOAnQxrcaWM-nvcABV7APWVQJ5rRtfqW=w1920-rw"
                }
            ]
        }
    }
}
</script>

<style scoped>
    .carousel img {
        width: 100%;
    }
    .lazyload .el-row {
        width: 85%;
        margin: 0 auto;
    }
    .lazyload .el-col {
        padding: 0 10px;
    }
    .lazyload {
        position: absolute;
        bottom: -60px;
        z-index: 100;
        width: 100%;
    }
    .lazyload-image img {
        border-radius: 10px;
        cursor: pointer;
    }
    .lazyload-image img:hover{
        object-fit: none;
    }
    .carousel {
        position: relative;
    }
</style>

<style>
    .carousel .el-carousel__item img {
        height: 100% !important;
        object-fit: cover !important;
    }
    .carousel .el-carousel__indicators {
        position: absolute;
        bottom: 100px;
    }
    .carousel .el-carousel {
        position: relative;
    }
</style>