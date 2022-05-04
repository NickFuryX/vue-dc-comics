<template>
  <div>
    <img src="../assets/img/dc-logo.png" alt="logo-dc">
    <nav>
      <ul>
        <li v-for="(item, index) in navItem" :key="index">{{item.nome}}</li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  data(){
    return{
      navItem: [
        {
          nome: "CHARACTERS",
          link: '#',
          stato: false,
        },
        {
          nome: "COMICS",
          link: '#',
          stato: true,
        },
        {
          nome: "MOVIES",
          link: '#',
          stato: false,
        },
        {
          nome: "TV",
          link: '#',
          stato: false,
        },
        {
          nome: "GAMES",
          link: '#',
          stato: false,
        },
        {
          nome: "COLLECTIBLES",
          link: '#',
          stato: false,
        },
        {
          nome: "VIDEOS",
          link: '#',
          stato: false,
        },
        {
          nome: "FANS",
          link: '#',
          stato: false,
        },
        {
          nome: "NEWS",
          link: '#',
          stato: false,
        },
        {
          nome: "SHOP",
          link: '#',
          stato: false,
        },
      ]
    }
  }
};
</script>

<style scoped lang="scss"></style>
