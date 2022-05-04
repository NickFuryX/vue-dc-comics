<template>
  <div class="main-container">
    <img src="../assets/img/dc-logo.png" alt="logo-dc" />
    <nav>
      <ul>
        <li @click="changeStatus" v-for="(item, index) in navItem" :key="index" :class="{'active': item.status}" >{{ item.nome }} </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      navItem: [
        {
          nome: "CHARACTERS",
          link: "#",
          stato: false,
        },
        {
          nome: "COMICS",
          link: "#",
          stato: true,
        },
        {
          nome: "MOVIES",
          link: "#",
          stato: false,
        },
        {
          nome: "TV",
          link: "#",
          stato: false,
        },
        {
          nome: "GAMES",
          link: "#",
          stato: false,
        },
        {
          nome: "COLLECTIBLES",
          link: "#",
          stato: false,
        },
        {
          nome: "VIDEOS",
          link: "#",
          stato: false,
        },
        {
          nome: "FANS",
          link: "#",
          stato: false,
        },
        {
          nome: "NEWS",
          link: "#",
          stato: false,
        },
        {
          nome: "SHOP",
          link: "#",
          stato: false,
        },
      ],
      methods: {
        changeStatus(){
          console.log('casa');
        },

      },
    };
  },
};
</script>

<style scoped lang="scss">
.main-container {
  height: 10vh;
  width: 100%;
  display: flex;
  justify-content: space-around;
  line-height: 5vh;
  padding-top: 10px;

  nav {
    height: 100%;
  }
  img {
    height: 100%;
  }

  ul {
    list-style-type: none;
    display: flex;
    height: 100%;

    li {
      padding: 0 10px 0 10px;
    }
  }
}
</style>
