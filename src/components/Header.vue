<template>
  <header class="vt-header">
    <div class="container-fluid">
      <nav class="navbar navbar-expand-lg">
        <a class="navbar-brand" href="#">
          <img src="@/assets/imgs/vt-logo.png" alt="">
        </a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
          <img src="@/assets/imgs/icons/vt-icon__menu.png" alt="">
        </button>
        <div class="collapse navbar-collapse" id="navbarNavDropdown">
          <ul class="navbar-nav">
            <li v-for="(item, index) in navItems" :key="index" class="nav-item">
              <a class="nav-link" href="#">{{ item.label }} <span class="border-btm"></span></a>
            </li>
          </ul>
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderVueTech',
  data() {
    return {
      navItems: [
        { label: 'Services' },
        { label: 'Choose Us' },
        { label: 'Prices' },
        { label: 'Contact' }
      ]
    }
  }
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

.vt-header{
  padding: 10px 0;
  font-size: 20px;
  border-bottom: 2px solid $vt-bg-light;

  .navbar-brand {
    margin-right: 14vw;
    img{
      height: 60px;
    }
  }

  .navbar-toggler{
    img{
      width: 40px;
    }
  }

  .collapse {
    &.navbar-collapse {
      .navbar-nav {
        gap: 40px;
        .nav-link {
          color: $vt-white;
          font-size: 20px;
          display: flex;
          flex-direction: column;
          
          .border-btm{
            height: 3px;
            background-color: none;
            width: 50%;
            margin: auto;
          }
          
          &:hover{
            .border-btm {
              background-color: $vt-yellow;
            }
          }
        }
        @media(max-width: 680px) {
          gap: 0;
        }
      }

    }
  }
}
</style>
