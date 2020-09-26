<template>
  <div id="app">
    <div class="header" :class="{ change_color_header: scrolled }">
      <div class="buttons">
        <span class="home_btn btn" @click="goHome()">home</span>
        <span class="about_btn btn" @click="goAbout()">about</span>
        <span class="experience_btn btn" @click="goExperience()">experience</span>
        <span class="networking_btn btn" @click="goNetworking()">networking</span>
        <span class="contacts_btn btn" @click="goContacts()">contacts</span>
      </div>
    </div>
    <Home class="home" />
    <About class="about" />
    <Experience class="experience" />
    <Networking class="networking" />
    <Contacts class="contacts" />
  </div>
</template>

<script>
import Home from "./components/Home.vue";
import About from "./components/About.vue";
import Experience from "./components/Experience.vue";
import Networking from "./components/Networking.vue";
import Contacts from "./components/Contacts.vue";

export default {
  name: "App",
  components: {
    Home,
    About,
    Experience,
    Networking,
    Contacts,
  },
  data() {
    return {
      scrolled: false,
    };
  },
  created() {
    window.addEventListener("scroll", this.changeColorHeader);
  },
  mounted() {
    document.querySelector(".home").scrollIntoView({ behavior: "smooth" });
  },
  methods: {
    changeColorHeader() {
      if (window.scrollY >= 50) {
        this.scrolled = true;
      } else {
        this.scrolled = false;
      }
    },
    goHome() {
      document.querySelector(".home").scrollIntoView({ behavior: "smooth" });
    },
    goAbout() {
      document.querySelector(".about").scrollIntoView({ behavior: "smooth" });
    },
    goExperience() {
      document.querySelector(".experience").scrollIntoView({ behavior: "smooth" });
    },
    goNetworking() {
      document.querySelector(".networking").scrollIntoView({ behavior: "smooth" });
    },
    goContacts() {
      document.querySelector(".contacts").scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
body {
  background-image: url(./assets/IMG_5617.png);
  background-attachment: fixed;
}
#app {
  display: grid;
  grid-template-rows: 1fr, 1fr, 1fr, 1fr, 1fr;
  justify-items: center;
  grid-template-areas:
    "header"
    "home"
    "about"
    "experience"
    "networking"
    "contacts";
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: graysca;
}
.header {
  position: fixed;
  grid-area: header;
  width: 100%;
  height: 50px;
  background-color: rgba(89, 107, 98, 0.85);
}
.change_color_header {
  background-color: rgba(89, 107, 98, 1);
}
.buttons {
  margin: auto;
  margin-top: 15px;
  width: 1024px;
  /* height: 100%; */
  color: rgb(199, 216, 208);
  font-weight: bold;
  text-align: right;
}
.btn {
  margin: 15px;
}
.btn:last-child {
  margin-right: 30px;
}
.btn:hover {
  color: rgb(183, 194, 188);
  cursor: pointer;
}
.home {
  grid-area: home;
}
.about {
  grid-area: about;
}
.experience {
  grid-area: experience;
}
.networking {
  grid-area: networking;
}
.contacts {
  grid-area: contacts;
}
</style>
