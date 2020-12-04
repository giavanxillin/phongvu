<template>
  <div class="header">
    <el-container>
      <el-main>
        <el-row class="header-row">
           <div class="header-wrapper">
            <div class="showroom"><i style="padding: 0 5px" class="el-icon-office-building"></i>Hệ thống showroom</div>
            <div class="consult"><i style="padding: 0 5px" class="el-icon-service"></i>Tư vấn mua hàng</div>
            <div><i style="padding: 0 5px" class="el-icon-service"></i>CSKH</div>
            <div><i  style="padding: 0 5px" class="el-icon-news"></i>Tin công nghệ</div>
            <div><i style="padding: 0 5px" class="el-icon-setting"></i>Xây dựng cấu hình</div>
        </div>
      </el-row>
       
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  background-color: #1435c3;
}
.header .el-main{
  padding: 10px 20px;
}
.header-row {
  display: flex;
  width: 90%;
  margin: 0 auto;
  justify-content: flex-end;
  
}
.header-wrapper{
  color: white;
  width: 60%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 14px;
  font-weight: 600;
}
</style>

