<template>
  <div class="experience">
    <div class="head">experience</div>
    <div class="layout"></div>
    <div class="web"></div>
  </div>
</template>

<script>
export default {
  name: "Experience",
};
</script>

<style scoped>
.experience {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-areas: "head layout web";
  width: 1024px;
  height: 400px;
  background-color: rgba(89, 107, 98, 1);
  color: rgb(199, 216, 208);
  align-items: center;
  justify-items: center;
}
.head {
  grid-area: head;
  font-size: 30px;
  font-weight: bold;
  justify-self: center;
  margin-left: 45px;
}
.layout {
  grid-area: layout;
  background-image: url(../assets/layout.png);
  background-size: 100% 100%;
  width: 250px;
  height: 250px;
}
.web {
  grid-area: web;
  background-image: url(../assets/web.png);
  background-size: 100% 100%;
  width: 250px;
  height: 250px;
}
@media all and (max-width: 800px) {
  .experience {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(2, 1fr);
    justify-items: center;
    align-items: center;
    grid-template-areas:
      "head head"
      "layout web";
    padding-bottom: 50px;
  }
  .head {
    margin-left: 0;
  }
}
</style>
