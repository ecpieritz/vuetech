
<template>
  <section class="vt-contact">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-9 col-md-7  col-12">
          <h2 class="mb-4">“Stand out online and make an impact”</h2>
          <p>Lisa Souza - CEO of a Tech Startup</p>
        </div>

        <div class="col-lg-3  col-md-5 col-12">
          <a class="vt-contact__btn" href="mailto: contact@vuetech.ag" target="_blank" rel="noopener noreferrer">Contact Us</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactVueTech",
};
</script>

<style scoped lang="scss">
$vt-bg: #2c2e33;
$vt-bg-light: #474a52;
$vt-black: #000000;
$vt-blue: #213e7a;
$vt-blue-dark: #122853;
$vt-grey: #cccbcb;
$vt-yellow: #ffa800;
$vt-yellow-dark: #d68f00;
$vt-white: #ffffff;

.vt-contact {
  background-color: $vt-blue;
  padding: 120px 0 40px;

  .row {
    row-gap: 20px;
    align-items: center;
  }

  &__btn{
    background-color: $vt-yellow;
    color: $vt-black;
    padding: 20px 40px;
    border-radius: 16px;
    font-size: 20px;
    text-decoration: none;

    &:hover {
      background-color: $vt-yellow-dark;
    }

  }

  @media(max-width: 460px) {
    padding: 80px 0;
    .col-lg-3{
      &.col-md-5{
        &.col-12 {
          text-align: center;
          margin: 40px 0 0;
        }
      }
    }
  }
}
</style>
