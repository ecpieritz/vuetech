<template>
  <main>
    <Header />
    <Banner />
    <Companies />
    <Services />
    <Choose />
    <WorkWith />
    <Prices />
    <Contact />
  </main>
</template>

<script>
import Header from "./components/Header.vue";
import Banner from "./components/Banner.vue";
import Companies from "./components/Companies.vue";
import Services from "./components/Services.vue";
import Choose from "./components/Choose.vue";
import WorkWith from "./components/WorkWith.vue";
import Prices from "./components/Prices.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "App",
  components: {
    Header,
    Banner,
    Companies,
    Services,
    Choose,
    WorkWith,
    Prices,
    Contact
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

// ----------
// Start Variables
// ----------
$vt-bg: #2c2e33;
$vt-black: #000000;
$vt-blue: #213e7a;
$vt-blue-dark: #122853;
$vt-grey: #cccbcb;
$vt-yellow: #ffa800;
$vt-yellow-dark: #d68f00;
$vt-white: #ffffff;
// ----------
// End Variables
// ----------

// ----------
// Start Default
// ----------
* {
  margin: 0;
  padding: 0;
  font-family: "Poppins", sans-serif;
}
body {
  background-color: $vt-bg;
  color: $vt-white;
}

.container-fluid {
  max-width: 1360px;

  padding: 0;

  @media(max-width: 1024px) {
    padding: 0 20px;
  }
}
// ----------
// End Default
// ----------

// ----------
// Start Texts
// ----------
h1 {
  font-size: 60px;
  line-height: 1.5;
  font-weight: 700;
}

h2 {
  font-size: 45px;
  line-height: 1.5;
  font-weight: 700;
}

h3 {
  font-size: 36px;
  line-height: 1.5;
  font-weight: 700;
}

h4 {
  font-size: 28px;
  line-height: 1.5;
  font-weight: 700;
}

p {
  font-size: 20px;
  line-height: 1.3;
  font-weight: 400;
}
a,
button {
  font-size: 16px;
  line-height: 1;
  font-weight: 700;
}

@media(max-width: 780px) {
  h1{
    font-size: 50px;
  }
  h2{
    font-size: 36px;
  }
  h3{
    font-size: 28px;
  }
  h4{
    font-size: 22px;
  }
}
// ----------
// End Texts
// ----------

// ----------
// Start Colors
// ----------
.vt-color {
  &__text {
    &__yellow {
      color: $vt-yellow;
    }
    &__black {
      color: $vt-black;
    }
  }

  &__bg {
    &__yellow {
      background-color: $vt-yellow;
    }
    &__blue {
      background-color: $vt-blue;
    }
  }
}
// ----------
// End Colors
// ----------

// ----------
// Start Btns
// ----------
.vt-btn {
  display: flex;
  align-items: center;
  text-transform: capitalize;
  padding: 20px 60px;
  border-radius: 16px;
  width: fit-content;
  &.yellow{
    background-color: $vt-yellow;
    color: $vt-black;
    
    &:hover{
      background-color: $vt-yellow-dark;
      color: $vt-white;
      text-decoration: none;
    }
  }

  &.white{
    background-color: $vt-white;
    color: $vt-blue;
    
    &:hover{
      background-color: $vt-grey;
      color: $vt-blue;
      text-decoration: none;
    }
  }

  @media(max-width: 780px) {
    padding: 20px 40px;
  }

  @media(max-width: 460px) {
    padding: 20px;
  }
}
// ----------
// End Btns
// ----------
</style>
