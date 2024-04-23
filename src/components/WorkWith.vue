
<template>
  <section class="vt-work">
    <div class="container-fluid">
      <h2 class="text-center mb-5">Work with VueTech</h2>

      <div class="row">
        <div v-for="(work, index) in works" :key="index" class="col-md-4 col-12">
          <div class="vt-work__card">
            <div class="vt-work__card__img">
              <img :src="work.icon" :alt="work.alt" />
            </div>

            <h3>{{ work.title }}</h3>
            <p><strong>{{ work.text }}</strong></p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "WorkWithVueTech",
  data() {
    return {
      works: [
        { icon: require('@/assets/imgs/icons/vt-icon__people.png'), alt: 'people', title: '10,000+', text: 'Happy Customers' },
        { icon: require('@/assets/imgs/icons/vt-icon__arrow-circle.png'), alt: 'arrow circle', title: '20,000+', text: 'Success Processes' },
        { icon: require('@/assets/imgs/icons/vt-icon__star.png'), alt: 'star', title: '10+ years', text: 'of Experience' },
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

.vt-work {
  background-color: $vt-blue;
  padding: 80px 0;

  .row {
    row-gap: 20px;
  }

  &__card {
    color: $vt-white;
    margin: auto;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 40px 20px;
    border-radius: 16px;
    height: 100%;

    &__img {
      width: 40%;
      margin: 0 auto 40px;
      background-color: $vt-yellow;
      padding: 30px;
      border-radius: 50%;

      img{
        width: 100%;
      }
    }
  }
}
</style>
