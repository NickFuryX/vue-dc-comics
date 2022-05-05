<template>
  <main>
    <div class="jumbotron"></div>
    <div class="container"></div>
  </main>
</template>

<script>
export default {
  name: "AppMain",
};
</script>

<style scoped lang="scss">
@import "../style/generals";
.jumbotron {
  width: 100%;
  height: 50vh;
  background-image: url("../assets/img/jumbotron.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
main {
  background: black;
  color: white;

  width: 100vw;
}
</style>
