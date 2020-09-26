<template>
  <div class="home">
    <div class="name_position">
      <div class="name">Anna Istratova</div>
      <div>Frontend devrloper</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped>
.home {
  display: grid;
  background-image: url(../assets/home_bacground.png);
  background-size: 100% 100%;
  width: 1024px;
  height: 475px;
  align-items: center;
}
.name_position {
  color: rgb(199, 216, 208);
  font-size: 50px;
  justify-self: start;
  margin-left: 30px;
}
.name {
  font-weight: bolder;
}
</style>
