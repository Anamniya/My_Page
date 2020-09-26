<template>
  <div class="contacts">
    <div class="head">Contacts</div>
    <div class="items">
      <div class="item"><span>telegram: @istratovaanna</span></div>
      <div class="item"><span>mail: ianna60c4@gmail.com</span></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contacts",
};
</script>

<style scoped>
.contacts {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 1024px;
  height: 250px;
  background-color: rgba(89, 107, 98, 1);
  color: rgb(199, 216, 208);
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
  grid-area: items;
  display: grid;
  grid-template-rows: repeat(2, 1fr);
  justify-self: center;
  align-self: center;
  font-size: 15px;
  grid-gap: 30px;
}
@media all and (max-width: 800px) {
  .contacts {
    grid-template-columns: 100%;
    grid-template-rows: repeat(3, 1fr);
    grid-template-areas: "head" "items";
    height: 200px;
  }
  .head {
    justify-self: center;
    margin-left: 0;
    padding-top: 25px;
  }
  .item {
    justify-self: center;
  }
  .item:first-child{
     padding-top: 25px;
  }
}
</style>
