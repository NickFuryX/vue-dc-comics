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
                <li>DC COMICS</li>
                <li>Characters</li>
                <li>Comics</li>
                <li>Movies</li>
                <li>Tv</li>
                <li>Games</li>
                <li>Videos</li>
                <li>News</li>
              </ul>
              <ul>
                <li>SHOP</li>
                <li>Shop DC</li>
                <li>Shop DC Collectables</li>
              </ul>
            </div>
            <div class="colonna2">
              <ul>
                <li>DC</li>
                <li>Terme Of Use</li>
                <li>Privacy Policy (New)</li>
                <li>Ad Choices</li>
                <li>Advertising</li>
                <li>Jobs</li>
                <li>Subscriptions</li>
                <li>Talent Workshops</li>
                <li>CPSC Certificates</li>
                <li>Ratings</li>
                <li>Shop Help</li>
                <li>Contact Us</li>
              </ul>
            </div>
            <div class="colonna3">
              <ul>
                <li>SITES</li>
                <li>DC</li>
                <li>MAD Magazine</li>
                <li>DC Kids</li>
                <li>DC Universe</li>
                <li>DC Power Visa</li>
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
          <div class="sign-btn">SIGN-UP NOW!</div>

          <div class="logo-follow">
            <div >FOLLOW US</div>
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
  overflow: hidden;
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
    color: grey;

    :first-child {
      font-size: 22px;
      padding: 10px 0 10px 0;
      font-weight: 900;
      color: white;
    }
  }
}

.footer-bottom-list-right {
  width: 50%;
  height: 100%;
  img {
    width: 80%;
    height: 80%;
    margin-top: -10%;
  }
}

.container-footer-bottom-list {
  display: flex;
}
.footer-bottom-social {
  width: 100%;
  height: 10vh;
  background-color: $gray-footer;
  display: flex;
  align-items: center;
  position: absolute;
  bottom: 0;
}
.container-footer-bottom-social {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo-follow {
  height: 100%;
  font-size: 20px;
  display: flex;
  align-items: center;
  color: $blue-color;
  font-weight: 900;
  column-gap: 10px;
  :first-child{
    padding-right: 20px;
  }
  img {
    width: 8%;
    height: 8%;
  }
}

.sign-btn {
  color: white;
  padding: 15px 40px 15px 40px;
  border: 3px solid $blue-color;  
}
</style>
