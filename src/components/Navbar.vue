<template>
    <div>
        <el-container>
            <el-main style="padding: 30px 20px">
                <el-row class="navbar-row">
                    <el-col :span="5" class=logo>
                        <img src="../assets/logo.svg" alt="">
                    </el-col>
                    <el-col :span="12" class="navbar-search">
                        <el-input
                            placeholder="Nhập từ khoá cần tìm"
                            suffix-icon="el-icon-search"
                            v-model="search">
                        </el-input>
                    </el-col>
                    <el-col :span="7">
                        <div class="select-wrapper">
                            <div class="promotion-item">
                                <i class="el-icon-discount"></i>
                                <div>Khuyến mãi</div>
                            </div>
                            <div class="order-item">
                                <i class="el-icon-document-checked"></i>
                                <div>Đơn hàng</div>
                            </div>
                            <div class="login-item">
                                <i class="el-icon-user"></i>
                                <div>Đăng nhập</div>
                            </div>
                            <div class="add-to-cart-item">
                                 <i class="el-icon-shopping-cart-2"></i>
                                <div>Giỏ hàng</div>
                            </div>
                        </div>
                    </el-col>
                </el-row>
            </el-main>
        </el-container>
    </div>
</template>

<script>
export default {
    data() {
        return {
            search: '',
        }
    }
}
</script>

<style scoped>
    .navbar-row {
        width: 90%;
        margin: 0 auto;
        display: flex;
        align-items: center;
    }
    .logo img {
        width: 100%;
    }
    .navbar-search {
        padding: 0 15px;
    }
    .select-wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-size: 12px;
    }
    .el-icon-discount {
        font-size: 25px;
    }
    .el-icon-document-checked {
        font-size: 25px;
    }
    .el-icon-user {
        font-size: 25px;
    }
    .el-icon-shopping-cart-2 {
        font-size: 25px;
    }
   

</style>