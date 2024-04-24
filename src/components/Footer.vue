<template>
  <section class="vt-footer">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-5 col-12 vt-footer__logo">
          <img class="mb-4" src="@/assets/imgs/vt-logo.png" alt="VueTech">
          <p>VueTech is a leading digital marketing agency dedicated to driving success for businesses online. With expertise in SEO, PPC, social media, content creation, and more, we offer tailored solutions to maximize ROI.</p>
        </div>

        <div class="col-md-2 col-6">
          <h4 class="mb-5">Our Services</h4>
          <ul>
            <li v-for="(service, index) in services" :key="index">{{ service }}</li>
          </ul>
        </div>

        <div class="col-md-2 col-6">
          <h4 class="mb-5">Explore More</h4>
          <ul>
            <li v-for="(link, index) in links" :key="index"><a :href="link.href">{{ link.title }}</a></li>
          </ul>
        </div>
        
        <div class="col-md-3 col-6">
          <h4 class="mb-5">Contact Us</h4>

          <div class="vt-footer__infos row">
            <div v-for="(info, index) in infos" :key="index" class="col-12">
              <div class="d-flex align-items-center">
                <div class="col-3">
                  <img :src="info.src" :alt="info.alt">
                </div>
                <div class="col-9">
                  <p>{{ info.text }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "FooterVueTech",
  data() {
    return {
      services: [
        "SEO Marketing",
        "Research Topic Trends",
        "Email Marketing",
        "Google PPC",
      ],
      links: [
        { href: '#vt-services', title: 'Services' },
        { href: '#vt-choose', title: 'Choose Us' },
        { href: '#vt-prices', title: 'Prices' },
        { href: '#vt-contact', title: 'Contact' },
        { href: '/', title: 'Privacy Policy' },
        { href: '/', title: 'Terms & Condition' },
      ],
      infos: [
        { src: require('@/assets/imgs/icons/vt-icon__local.png'), alt: 'local', text: '5th Street, Ananindeua - Brazil' },
        { src: require('@/assets/imgs/icons/vt-icon__phone.png'), alt: 'phone', text: '+55 91 3456-7891' },
        { src: require('@/assets/imgs/icons/vt-icon__cellphone.png'), alt: 'cellphone', text: '+55 91 98765-4321' },
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

.vt-footer {
  color: $vt-white;
  padding: 80px 0 0;

  &__logo{
    img{
      width: 37%;
    }
  }

  h4{
    color: $vt-yellow;
  }

  ul{
    list-style-type: none; 
    li{
      font-size: 20px;
      margin-bottom: 5px;
      a{
        font-size: 20px;
        font-weight: 400;
        color: $vt-white;
        text-decoration: none;
        &:hover {
          color: $vt-yellow;
        }
      }
    }
  }

  &__infos{

    .col-12{
      margin-bottom: 20px;

      p{
        margin: 0;
      }
    }
    img{
      width: 100%;
    }
  }
}
</style>
