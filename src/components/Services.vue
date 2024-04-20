<template>
  <section class="vt-companies">
    <div class="container-fluid">
      <h2 class="text-center">Services</h2>
      <p class="text-center mb-5">
        Strategic services drive digital success with tailored, comprehensive approaches.
      </p>

      <div class="row">
        <div class="col-md-3 col-sm-6 col-12">
          <div class="vt-companies__card">
            <img src="@/assets/imgs/icons/vt-icon__seo.png" alt="seo notebook" />
            <p><strong>SEO Marketing</strong></p>
          </div>
        </div>

        <div class="col-md-3 col-sm-6 col-12">
          <div class="vt-companies__card">
            <img src="@/assets/imgs/icons/vt-icon__research.png" alt="research topic graphs" />
            <p><strong>Research Topic Trends</strong></p>
          </div>
        </div>

        <div class="col-md-3 col-sm-6 col-12">
          <div class="vt-companies__card">
            <img src="@/assets/imgs/icons/vt-icon__email.png" alt="email" />
            <p><strong>Email Marketing</strong></p>
          </div>
        </div>

        <div class="col-md-3 col-sm-6 col-12">
          <div class="vt-companies__card">
            <img src="@/assets/imgs/icons/vt-icon__ppc.png" alt="money screen topics" />
            <p><strong>Google PPC</strong></p>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ServicesVueTech",
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

.vt-companies {
  background-color: $vt-blue;
  padding: 80px 0;

  .row {
    row-gap: 20px;
  }

  &__card {
    background-color: $vt-yellow;
    color: $vt-black;
    margin: auto;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 40px 20px;
    border-radius: 16px;
    height: 100%;

    img {
      width: 40%;
      margin-bottom: 40px;
    }
  }
}
</style>
