<template>
  <div class="container">
    <div class="header-container">
      <img src="../assets/img/dc-logo.png" alt="logo-dc" />
      <nav>
        <ul>
          <li
            @click="changeStatus(index)"
            v-for="(item, index) in navItem"
            :key="index"
            :class="{ active: item.stato }"
          >
            {{ item.nome }}
          </li>
        </ul>
      </nav>
    </div>
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
    };
  },
  methods: {
    changeStatus(index) {
      for (let i = 0; i < this.navItem.length; i++) {
        this.navItem[i].stato = false;
      }

      this.navItem[index].stato = !this.navItem[index].stato;
    },
  },
};
</script>

<style lang="scss">
@import "../style/generals";
.header-container {
  height: 15vh;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;

  nav {
    height: 100%;
  }
  img {
    height: 70%;
  }

  ul {
    list-style-type: none;
    display: flex;
    align-items: center;
    height: 100%;

    li {
      padding: 0 10px 0 10px;
      height: 100%;
      display: flex;
      align-items: center;
    }
  }
  .active {
    color: $blue-color;
    border-bottom: 4px solid $blue-color;
  }
}
</style>
