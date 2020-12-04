<template>
  <div class="product" style="margin-top:70px">
    <div class="product-bar">

        <el-col :span="12">
          <div class="grid-content bg-purple">
            <!-- Laptop button -->
          <button style="width:100%" >
            <div  data-track-content="true" data-content-region-name="hotDealTab" data-content-name="Tuần lễ Laptop">
              <div>Tuần lễ Laptop</div>
              <div>Giá shock - giảm tới 2.3 triệu</div>
              </div>
          </button>
          </div>
          </el-col>
  
        <el-col :span="12">
          <div class="grid-content bg-purple">
      <!-- Smart Phone Button -->
      <button style="width:100%">
        <div  data-track-content="true" data-content-region-name="hotDealTab" data-content-name="SmartPhone">
          <div>Điện Thoại</div>
          <div>Giá shock - giảm tới 2.3 triệu</div>
        </div>
      </button>
       </div>
       </el-col>
    </div>
    <div style="text-align: right">
      <a href="" style="color:white">Xem tất cả ></a>
    <hr/>
    </div>

    <el-container>
      <el-aside width="260px">
                  <img class="image" src="../assets/background/laptop.jpg" alt="LAPTOP - MACBOOK">      </el-aside>
      <el-main>
    <div id="product-slider">
      <section>
        <vue-horizontal-list :items="items" :options="options">
          <template v-slot:default="{ item }">
            <div class="item">
              <img v-bind:src="item.image" alt="" class="item-img" />
              <p>{{ item.title }}</p>
              <div class="price">
                <span>{{ item.price }}</span>
              </div>
              <div class="old-price">
                <span
                  ><strike>{{ item.oldPrice }}</strike></span
                >
              </div>
            </div>
          </template>
        </vue-horizontal-list>
      </section>
    </div>
    </el-main>
</el-container>
  </div>
</template>

<script>
import Vue from "vue";
import VueHorizontalList from "../../node_modules/vue-horizontal-list/src/vue-horizontal-list";

export default Vue.extend({
  name: "ServeDev",
  components: {
    VueHorizontalList,
  },
  data() {
    return {
      options: {
        responsive: [
            { end: 192, size: 1 },
            { start: 384, end: 576, size: 2 },
            { start: 576, end: 768, size: 3 },
            { start: 768, end: 960, size: 4 },
            { start: 1152, size: 5 },
        ],
        list: {
          // 1200 because @media (min-width: 1200px) and therefore I want to switch to windowed mode
          windowed: 1200,

          // Because: #app {padding: 80px 24px;}
          padding: 24,
        },
      },
      items: [
        {
          title: 'Màn Hình Dell Ultrasharp 24" U2419H (1920x1080/IPS/60Hz/8ms)',
          image: require("../assets/Product/dell-ultrasharp.webp"),
          oldPrice: "5.690.000",
          price: "5.189.000",
        },
        {
          title:
            'Laptop ASUS VivoBook 14 A412FA-EK734T (14" FHD/i5-10210U/8GB/512GB SSD/Intel UHD/Win10/1.5kg)',
          image: require("../assets/Product/asus1.webp"),
          oldPrice: "15.690.000",
          price: "15.189.000",
        },
        {
          title:
            'Laptop ASUS VivoBook 14 A412FA-EK734T (14" FHD/i5-10210U/8GB/512GB SSD/Intel UHD/Win10/1.5kg)',
          image: require("../assets/Product/asus-2.webp"),
          oldPrice: "15.690.000",
          price: "15.189.000",
        },
        {
          title:
            'Laptop ASUS VivoBook 14 A412FA-EK734T (14" FHD/i5-10210U/8GB/512GB SSD/Intel UHD/Win10/1.5kg)',
          image: require("../assets/Product/asus-3.webp"),
          oldPrice: "15.690.000",
          price: "15.189.000",
        },
        {
          title:
            'Laptop ASUS VivoBook 14 A412FA-EK734T (14" FHD/i5-10210U/8GB/512GB SSD/Intel UHD/Win10/1.5kg)',
          image: require("../assets/Product/dell-vostro.webp"),
          oldPrice: "15.690.000",
          price: "15.189.000",
        },
        {
          title:
            'Laptop ASUS VivoBook 14 A412FA-EK734T (14" FHD/i5-10210U/8GB/512GB SSD/Intel UHD/Win10/1.5kg)',
          image: require("../assets/Product/macair.png"),
          oldPrice: "15.690.000",
          price: "15.189.000",
        },
      ],
    };
  },
});
</script>

<style scoped>
.container{
  margin: 0 20px;
}
button:hover{
  font-weight: bold;
  background-color: #00008B;
  color: white;
}
button{
  cursor: pointer;
  border-radius: 0.5rem;
  display: block;
  font-size: 20px;
}
hr{
  margin: 0 !important;
}
.product-bar{
display: flex;
justify-content: center;
align-items: center;
height: 60px;

}
/* .product-bar h3 {
  color: white;
  display: inline;
  margin: 0 30px;
  line-height: 60px;
  font-size: 20px;
}
.product-bar a{
  display: inline;
  text-align: right;
  margin-right: 25px;
  line-height: 60px;
  color: white;
  text-decoration: none;
  font-size: 13px;
} */
#product-slider {
  padding-left: 50px;
}
.price {
  font-size: 18px;
  font-weight: bold;
  color: blue;
}
.item {
  max-width: 200px;
  font-size: 14px;
  background-color: rgb(255, 255, 255);
  padding: 0.3rem;
  max-height: 400px;
  min-height: 416.09px;
  border-radius: 0.5rem;
  text-align: center;
  cursor: pointer;
  display: block;
  text-decoration: none;
  color: rgb(51, 51, 51);
  height: 100%;

}
.product {
  background-image: url("../assets/background/background.jpg"); 
  background-repeat: no-repeat;
  background-size: cover;
  /* padding-top: 50px; */
}
.item-img {
  max-width: 170px;
  max-height: 170px;
}
body {
  margin: 0;
  padding: 0;
}

#app {
  max-width: 1400px;

  margin-left: auto;
  margin-right: auto;

  padding: 80px 24px;
}

@media (min-width: 1200px) {
  #app {
    padding-left: 80px;
    padding-right: 80px;
  }
}
</style>
