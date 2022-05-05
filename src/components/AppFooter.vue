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
      <div class="footer-bottom-list">
        <div class="container container-footer-bottom-list">
          <div class="footer-bottom-list-left">
            <div class="colonna1">
              <ul>
                DC COMICS
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
              </ul>
              <ul>
                SHOP
                <li>FFF</li>
                <li>FFF</li>
              </ul>
            </div>
            <div class="colonna2">
              <ul>
                DC
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
              </ul>
            </div>
            <div class="colonna3">
              <ul>
                SITES
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
                <li>FFF</li>
              </ul>
            </div>
          </div>
          <div class="footer-bottom-list-right">
            <img src="../assets/img/dc-logo-bg.png" alt="" />
          </div>
        </div>
      </div>
      <div class="footer-bottom-social">
        <div class="container container-footer-bottom-social">
          <div>SIGN-UP</div>

          <div class="logo-follow">
              <div>FOLLOW US</div>
              <img src="../assets/img/footer-facebook.png" alt="" />
              <img src="../assets/img/footer-twitter.png" alt="" />
              <img src="../assets/img/footer-youtube.png" alt="" />
              <img src="../assets/img/footer-pinterest.png" alt="" />
              <img src="../assets/img/footer-periscope.png" alt="" />
          </div>
        </div>
      </div>
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
.footer-bottom {
  position: relative;
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

.footer-bottom-list-left {
  color: white;
  width: 50%;
  height: 100%;
  padding-top: 30px;
  column-gap: 30px;
  display: flex;

  ul {
    list-style-type: none;
  }
}

.footer-bottom-list-right {
  width: 50%;
  height: 100%;
  img {
    width: 100%;
    height: 100%;
  }
}

.container-footer-bottom-list {
  display: flex;
}
.footer-bottom-social {
  width: 100%;
  height: 10vh;
  background-color: $gray-footer;
  position: absolute;
  bottom: 0;
  display: flex;
  align-items: center;
}
.container-footer-bottom-social {
  display: flex;
  justify-content: space-between;

}
.logo-follow{
    height: 100%;
    font-size: 20px;
    display: flex;
  align-items: center;
  img{
      width: 8%;
      height: 8%;
      
  }
}
</style>
