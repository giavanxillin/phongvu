<template>
  <div class="SuggestedItems">
    <div class="suggested-item-title">
      <h3><b>Dành cho bạn</b></h3>
    </div>
    <hr />
    <div id="suggested-item-slider">
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
          { end: 576, size: 1 },
          { start: 576, end: 768, size: 2 },
          { start: 768, end: 992, size: 4 },
          { size: 5 },
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
/* .container{
  margin: 0 20px;
} */
hr{
  margin: 0 !important;
}
.SuggestedItems {
padding: 10px;
}
.suggested-item-title {
display: flex;
justify-content: space-between;
align-items: center;
height: 60px;
margin-top: 30px;
}
.suggested-item-title h3 {
  color: black;
  display: inline;
  margin: 0 30px;
  line-height: 60px;
  font-size: 20px;
}
#suggested-item-slider {
  padding: 0 40px;
}
.price {
  font-size: 18px;
  font-weight: bold;
  color: blue;
}
.item {
  width: fit-content;
  font-size: 13px;
  background-color: white;
  padding: 15px;
  max-height: 400px;
  min-height: 350px;
  border-radius: 15px;
  text-align: left;
}
.suggested-item {
  background-image: url("../assets/Product/unnamed.png");
  background-repeat: no-repeat;
  background-size: cover;

  /* background-position: center; */
}
.item-img {
  max-width: 200px;
  max-height: 300px;
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
