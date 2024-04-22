<template>
  <section class="vt-choose">
    <div class="container-fluid">
      <div class="vt-choose__title">
        <h3 class="mb-5">Why Choose Us?</h3>
        <div class="vt-choose__title__bar"></div>
      </div>

      <div
        v-for="(row, index) in rows"
        :key="index"
        :class="['row', index % 2 === 0 ? '' : 'row-inverse']"
      >
        <div class="col-md-5">
          <img :src="row.image" :alt="row.alt" />
        </div>
        <div class="col-md-7">
          <h2>{{ row.title }}</h2>
          <p>{{ row.text }}</p>

          <a
            class="vt-btn yellow"
            href="{{row.href}}"
            target="_blank"
            rel="noopener noreferrer"
            >Learn More</a
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ChooseVueTech",
  data() {
    return {
      rows: [
        {
          image: require("@/assets/imgs/vt-choose__img-01.png"),
          alt: "2 persons reading",
          title: "Solutions Tailored Specifically to Your Business Needs",
          text:
            "We provide customized solutions for your business needs, ensuring relevance and success.",
          href: "/",
        },
        {
          image: require("@/assets/imgs/vt-choose__img-02.png"),
          alt: "3 persons in front of a pc",
          title: "Creative Excellence Elevates Every Project",
          text:
            "Creative excellence drives our work. From concept to execution, we aim for exceptional results.",
          href: "/",
        },
        {
          image: require("@/assets/imgs/vt-choose__img-03.png"),
          alt: "2 men shaking hands",
          title: "Client Satisfaction is Our Main Focus",
          text:
            "Our main goal is your satisfaction, and we work tirelessly to ensure that you are pleased with the results we achieve together.",
          href: "/",
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

.vt-choose {
  padding: 80px 0;

  &__title {
    display: flex;
    align-items: center;
    gap: 20px;

    &__bar {
      height: 3px;
      width: 15rem;
      background-color: $vt-white;
    }

    h3{
      line-height: 1;
    }
  }

  .row {
    margin-bottom: 80px;

    .col-md-7 {
      padding-left: 80px;

      h2 {
        width: 80%;
      }

      p {
        width: 80%;
        margin: 20px 0 50px;
        font-size: 24px;
      }

    }
  }

  .row-inverse {
    margin-bottom: 80px;
    flex-direction: row-reverse;

    .col-md-7 {
      text-align: end;
      padding-right: 80px;

      h2 {
        width: 80%;
        margin-left: auto;
      }
      p {
        width: 80%;
        margin: 20px 0 50px;
        margin-left: auto;
        font-size: 24px;
      }
      .vt-btn {
        margin-left: auto;
      }

    }

  }

  img {
    width: 100%;
  }

}
</style>
