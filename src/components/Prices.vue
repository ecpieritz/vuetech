<template>
  <section class="vt-prices">
    <div class="container-fluid">
      <h2 class="text-center">Pricing Plans</h2>
      <p class="text-center mb-5">The Best Solution for Our Clients</p>

      <div class="row">
        <div v-for="(price, index) in prices" :key="index" class="col-md-4 col-12">
          <div class="vt-prices__card">
            <h4>{{ price.title }}</h4>
            <h2>{{ price.price }}</h2>

            <ul class="vt-prices__card__list">
              <li v-for="(info, infoIndex) in price.infos" :key="infoIndex">
                {{ info }}
              </li>
            </ul>

            <a class="vt-prices__card__btn" href="/">Book Now</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "PricesVueTech",
  data() {
    return {
      prices: [
        {
          title: "Starter Plan",
          price: "$500",
          infos: [
            "Responsive website design and development (5 pages)",
            "Basic SEO",
            "Social media management",
            "Ideal for small business"
          ],
        },
        {
          title: "Business  Plan",
          price: "$1000",
          infos: [
            "Responsive website design and development (10 pages)",
            "Advanced SEO",
            "Social media management",
            "PPC advertising campaign ",
          ],
        },
        {
          title: "Premium Plan",
          price: "$2000",
          infos: [
            "Advanced Business plan",
            "Regular content creation",
            "Performance analysis and monthly reporting",
            "Email marketing"
          ],
        },
      ],
    };
  },
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

.vt-prices {
  background-color: $vt-yellow;
  padding: 80px 0;

  .row {
    row-gap: 20px;
  }

  &__card {
    background-color: $vt-blue;
    color: $vt-white;
    margin: auto;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 40px 20px;
    border-radius: 16px;
    height: 100%;

    &__list{
      width: 100%;
      text-align: left;
      padding: 10px 40px 40px;
      font-size: 20px;
    }

    &__btn {
      background-color: $vt-yellow;
      color: $vt-black;
      font-size: 18px;
      padding: 10px 20px;
      border-radius: 16px;
      text-decoration: none;

      &:hover {
        background-color: $vt-yellow-dark;
      }
    }
  }
}
</style>
