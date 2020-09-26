<template>
  <div class="networking">
    <div class="head">Networking</div>
      <div class="items">
        <a href="https://github.com/Anamniya">
          <div class="item github"></div>
        </a>
        <a href="https://www.linkedin.com/in/anna-istratova-37a06b91/">
          <div class="item linkedin"></div>
        </a>
        <a href="https://career.habr.com/annaistratova">
          <div class="item habr"></div>
        </a>
      </div>
  </div>
</template>

<script>
export default {
  name: "Networking",
};
</script>

<style scoped>
.networking {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 1024px;
  height: 250px;
  background-color: rgba(167, 204, 186, 0.2);
  color: rgb(43, 56, 50);
  grid-template-areas: "head items";
}
.head {
  grid-area: head;
  justify-self: start;
  align-self: center;
  font-size: 30px;
  font-weight: bold;
  margin-left: 115px;
}
.items {
  display: grid;
  grid-area: items;
  grid-template-columns: repeat(3, 1fr);
  justify-items: center;
  align-items: center;
  grid-gap: 50px;
  height: 250px;
  width: 512px;
  background: rgba(89, 107, 98, 0.5);
}
.item {
  width: 50px;
  height: 50px;
}
.item.linkedin {
  width: 58.8px;
  height: 50px;
}
.item:hover {
  opacity: 0.85;
}
.github {
  background-image: url(../assets/github.png);
  background-size: 100% 100%;
}
.linkedin {
  background-image: url(../assets/linkedin.png);
  background-size: 100% 100%;
}
.habr {
  background-image: url(../assets/habr.png);
  background-size: 100% 100%;
}
@media all and (max-width: 800px) {
  .networking {
    grid-template-columns: 100%;
    grid-template-rows: repeat(2, 1fr);
    grid-template-areas:
      "head"
      "items";
  }
  .head {
    margin-left: 0;
    justify-self: center;
    align-self: center;
    padding-top: 50px;
    height: 75px;
  }
  .items {
    width: 100%;
    height: 125px;
  }
}
</style>
