<template>
  <section class="vt-companies">
    <div class="container-fluid">
      <h3 class="text-center mb-5">Trusted by thousand companies </h3>

      <div class="row">
        <div v-for="(company, index) in companies" :key="index" class="col">
          <img :src="company.image" :alt="company.alt">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "CompaniesrVueTech",
  data() {
    return {
      companies: [
        { image: require('@/assets/imgs/vt-companies__pinterest.png'), alt: 'Pinterest' },
        { image: require('@/assets/imgs/vt-companies__google.png'), alt: 'Google' },
        { image: require('@/assets/imgs/vt-companies__neon.png'), alt: 'Neon' },
        { image: require('@/assets/imgs/vt-companies__shopee.png'), alt: 'Shopee' },
        { image: require('@/assets/imgs/vt-companies__unilever.png'), alt: 'Unilever' },
        { image: require('@/assets/imgs/vt-companies__spotify.png'), alt: 'Spotify' },
        { image: require('@/assets/imgs/vt-companies__trip.png'), alt: 'Trip Adviser' },
        { image: require('@/assets/imgs/vt-companies__grab.png'), alt: 'Grab' },
        { image: require('@/assets/imgs/vt-companies__airbnb.png'), alt: 'Airbnb' }
      ]
    };
  }
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
  background-color: $vt-yellow;
  padding: 40px 0;
  color: $vt-black;

  .row{
    row-gap: 20px;
    .col{
      display: flex;
      justify-content: center;
      img{
        width: 80px;
      }
    }
  }
  
  @media (max-width: 1024px) {
    .row{
      .col{
        img{
          width: 60px;
        }
      }
    }
  }
  
  @media (max-width: 780px) {
    padding: 40px 0;
    
    .row{
      justify-content: center;
      margin: auto;
      .col{
        min-width: 20% !important;
        max-width: 20% !important;
      }
    }
  }

  @media (max-width: 460px) {
    .row{
      .col{
        min-width: 30% !important;
        max-width: 30% !important;
      }
    }
  }
}
</style>
