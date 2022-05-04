<template>
  <footer>
    <div class="footer-top">
      <div class="container container-footer-top">
        <div class="card-box" v-for="(item, index) in card" :key="index">
          <img :src="item.source" alt="" />
          <div>{{ item.nome }}</div>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="footer-bottom-list"></div>
      <div class="footer-bottom-social"></div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  data() {
    return {
      card: [
        {
          nome: "DIGITAL COMICS",
          source: require("../assets/img/buy-comics-digital-comics.png"),
        },
        {
          nome: "DC MERCHANDISE",
          source: require("../assets/img/buy-comics-merchandise.png"),
        },
        {
          nome: "SUBSCRIPTION",
          source: require("../assets/img/buy-comics-subscriptions.png"),
        },
        {
          nome: "COMICS SHOP LOCATION",
          source: require("../assets/img/buy-comics-shop-locator.png"),
        },
        {
          nome: "DC POWER VISA",
          source: require("../assets/img/buy-dc-power-visa.svg"),
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../style/generals";
.footer-top {
  background-color: $blue-color;
  height: 20vh;
}
.container-footer-top {
  height: 100%;
  display: flex;
  justify-content: center;
  column-gap: 40px;
}
img {
  height: 30%;
  margin-right: 10px;
}
.card-box {
  height: 100%;
  display: flex;
  align-items: center;
  font-size: 12px;
  color: white;
}
.footer-bottom-list {
  width: 100%;
  height: 50vh;
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
