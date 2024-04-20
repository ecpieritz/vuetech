<template>
  <section class="vt-banner">
    <div class="container-fluid">
      <div class="d-flex flex-column">
        <h1><span class="vt-color__text__yellow">Boost</span> Your Brand with Innovative <span class="vt-color__text__yellow">Digital Marketing</span></h1>
      <p>Drive Engagement and Conversions with Advanced Digital Marketing Strategies.</p>
      <div class="d-flex">
        <a href="#contact" class="vt-btn yellow">Start Now</a>
        <a href="https://youtu.be/IjS9eTpmhgk?si=roSQl5yLghGs9NaH" target="_blank" class="vt-btn white">
          <img src="@/assets/imgs/icons/vt-icon__play.png" alt="play icon">
          Watch Demo
        </a>
      </div>
      </div>
    </div>
  </section>

</template>

<script>
export default {
  name: 'BannerVueTech',
}
</script>

<style scoped lang="scss">
$vt-bg: #2C2E33;
$vt-bg-light: #474a52;
$vt-black: #000000;
$vt-blue: #213E7A;
$vt-blue-dark: #122853;
$vt-grey: #cccbcb;
$vt-yellow: #FFA800;
$vt-yellow-dark: #d68f00;
$vt-white: #ffffff;

.vt-banner{
  padding: 40px 0;
  .container-fluid{
    background-image: url('@/assets/imgs/vt-home__banner-img.png');
    background-position: top center;
    background-repeat: no-repeat;
    background-size: 100%;
    height: 650px;

    .d-flex{
      gap: 20px;
      width: 100%;

      &.flex-column{
        width: 50%;
      }

      .vt-btn{
        img{
          width: 24px;
        }
      }
    }

    @media(max-width: 780px){
      .d-flex{
        &.flex-column{
          width: 65%;
        }
      }
    }

    @media(max-width: 460px){
      background-image: none;
      .d-flex{
        &.flex-column{
          width: 100%;
        }
      }
    }
  }
}
</style>
