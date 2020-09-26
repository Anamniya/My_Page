<template>
  <div class="about">
    <div class="head">About</div>
    <div class="text">
      Hi! My name is Anna.
      <br />I'm a frontend developer.
      <br />I have the knowlage to created beatuful fhings for you.
      <br />If you need it, text me.
      <br />Contacts at the bottom of this page.
    </div>
    <div class="graphs">
      <div class="html">
        <div class="knowlage_text">HTML</div>
        <div class="knowlage_graph html_graph"></div>
      </div>
      <div class="css">
        <div class="knowlage_text">CSS</div>
        <div class="knowlage_graph css_graph"></div>
      </div>
      <div class="bootstrap">
        <div class="knowlage_text">Bootstrap</div>
        <div class="knowlage_graph bootstrap_graph"></div>
      </div>
      <div class="javascript">
        <div class="knowlage_text">JavaScript</div>
        <div class="knowlage_graph javascript_graph"></div>
      </div>
      <div class="vue">
        <div class="knowlage_text">Vue</div>
        <div class="knowlage_graph vue_graph"></div>
      </div>
      <div class="react">
        <div class="knowlage_text">React</div>
        <div class="knowlage_graph react_graph"></div>
      </div>
      <div class="angular">
        <div class="knowlage_text">Angular</div>
        <div class="knowlage_graph angular_graph"></div>
      </div>
      <div class="jquery">
        <div class="knowlage_text">jQuery</div>
        <div class="knowlage_graph jquery_graph"></div>
      </div>
      <div class="sql">
        <div class="knowlage_text">SQL</div>
        <div class="knowlage_graph sql_graph"></div>
      </div>
      <div class="git">
        <div class="knowlage_text">Git</div>
        <div class="knowlage_graph git_graph"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
.about {
  display: grid;
  grid-template-rows: 2fr 5fr;
  grid-template-columns: 1fr 2fr;
  grid-template-areas:
    "head text"
    "head graphs";
  width: 1024px;
  height: 900px;
  background-color: rgba(167, 204, 186, 0.2);
  color: rgb(43, 56, 50);
}
.head {
  grid-area: head;
  justify-self: center;
  align-self: center;
  font-size: 30px;
  font-weight: bold;
}
.text {
  grid-area: text;
  justify-self: center;
  align-self: center;
  font-size: 20px;
}
.graphs {
  grid-area: graphs;
  justify-self: center;
  align-self: center;
}
.knowlage_graph {
  width: 500px;
  height: 10px;
  margin-top: 5px;
}
.knowlage_text {
  font-size: 15px;
  font-weight: bold;
  margin-top: 15px;
}
.html_graph {
  background-image: url(../assets/450px.png);
  background-size: 100% 100%;
}
.css_graph {
  background-image: url(../assets/400px.png);
  background-size: 100% 100%;
}
.bootstrap_graph {
  background-image: url(../assets/400px.png);
  background-size: 100% 100%;
}
.javascript_graph {
  background-image: url(../assets/350px.png);
  background-size: 100% 100%;
}
.vue_graph {
  background-image: url(../assets/250px.png);
  background-size: 100% 100%;
}
.react_graph {
  background-image: url(../assets/200px.png);
  background-size: 100% 100%;
}
.angular_graph {
  background-image: url(../assets/200px.png);
  background-size: 100% 100%;
}
.jquery_graph {
  background-image: url(../assets/350px.png);
  background-size: 100% 100%;
}
.sql_graph {
  background-image: url(../assets/250px.png);
  background-size: 100% 100%;
}
.git_graph {
  background-image: url(../assets/250px.png);
  background-size: 100% 100%;
}

@media all and (max-width: 800px) {
  .about {
    grid-template-columns: 100%;
    justify-items: center;
    align-items: center;
    grid-template-areas:
      "head"
      "text"
      "graphs";
    height: 800px;
    padding-bottom: 50px;
    padding-top: 50px;
  }
  .text {
    justify-self: center;
    margin-top: 0;
  }
  .graphs {
    justify-self: center;
    margin-top: 50px;
  }
}
</style>
