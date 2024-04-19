<template>
  <main>
    <Header />

  </main>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

$vt-bg: #2C2E33;
$vt-black: #000000;
$vt-blue: #213E7A;
$vt-blue-dark: #122853;
$vt-grey: #cccbcb;
$vt-yellow: #FFA800;
$vt-yellow-dark: #d68f00;
$vt-white: #ffffff;

*{
  margin: 0;
  padding: 0;
  font-family: "Poppins", sans-serif;
}
body{
  background-color: $vt-bg;
  color: $vt-white;
}

.container-fluid{
  max-width: 1360px;
}
</style>
