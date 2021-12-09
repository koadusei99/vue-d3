<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Navbar />
    <section class="hero">
      <h1>Don't Buy Fear</h1>
      <p>It go cost you</p>
    </section>
    <Pricing :prices="prices" />
    <Sponsors :sponsors="sponsors"></Sponsors>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Navbar from "./components/Navbar.vue";
import Pricing from "./components/Pricing.vue";
import Sponsors from "./components/Sponsors.vue";

let prices = [
  {
    id: 12,
    category: "Consecter",
    desc: "Animi corrupti nulla",
    price: 100,
    mollitia: 150,
    laudantium: 50,
    excepturi: 8,
  },
  {
    id: 64,
    category: "mollitia",
    desc: "adipisci eveniet suscipit",
    price: 250,
    mollitia: 350,
    laudantium: 200,
    excepturi: 25,
  },
  {
    id: 123,
    category: "adipisicing",
    desc: " autem, vero magnam hic",
    price: 450,
    mollitia: 600,
    laudantium: 400,
    excepturi: 250,
  },
];
let sponsors = [
  {
    id: 0,
    name: "Daverose Musuruba",
    img: "daver.png",
    pos: "CEO",
    org: "Musumetics",
  },
  {
    id: 1,
    name: "Papa Yaw Agyekum Addo",
    img: "papa.png",
    pos: "Chief Chemist",
    org: "Kofikrom Pharma",
  },
  {
    id: 2,
    name: "David G Lover",
    img: "dav.png",
    pos: "CTO",
    org: "Lover Inc",
  },
  {
    id: 3,
    name: "Mark Wamoah",
    img: "mark.png",
    pos: "CEO",
    org: "Amoah Construction",
  },
];
export default {
  name: "App",
  components: {
    Navbar,
    Pricing,
    Sponsors,
  },
  data() {
    return {
      prices,
      sponsors,
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
#app {
  font-family: Karla, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.hero {
  background-image: url("./assets/hero.png");
  background-size: cover;
  min-height: 100vh;
  position: relative;
  font-family: Barlow;
}
.hero::after {
  content: "";
  position: absolute;
  inset: 0;
  background-color: rgba(255, 34, 0, 0.3);
}
.hero h1 {
  font-size: 3rem;
  font-weight: 800;
}
.hero p {
  font-size: 3rem;
  font-weight: 800;
}
.btn {
  border: 1px solid red;
  padding: 0.8rem 1.5rem;
  font-size: 1rem;
  font-weight: 600;
  font-family: Barlow;
  background-color: white;
  color: red;
  border-radius: 5px;
}
</style>
