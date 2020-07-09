<template>
  <section class="headline">
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <h1>PHP Hosting</h1>
          <h2>Cepat, handal, penuh dengan modul PHP yang Anda Butuhkan</h2>
          <ul class="headline__list">
            <li v-for="(mod, index) in modules" :key="index">{{mod}}</li>
          </ul>
        </div>
        <div class="col-md-6">
          <img class="img-fluid" src="@/assets/icon/banner.svg" alt="">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Headline',
  data() {
    return {
      modules: [
        'Solusi PHP untuk performa query yang lebih cepat',
        'Konsumsi memori yang lebih rendah',
        'support PHP 5.3. PHP 5.4, PHP 5.5, PHP 5.6, PHP 7',
        'Fitur enkripsi ionCube dan Zend Guard Loaders'
      ]
    }
  }
}
</script>

<style lang="scss">
.headline {
  @extend %main-separator--bottom;

  padding-top: 50px;
  padding-bottom: 50px;

  h1 {
    @extend %montserrat;
    font-weight: bold;
  }
  h2 {
    font-weight: 200;
    margin-bottom: 25px;
  }
  &__list {
    @extend .icon-list;
  }
}
</style>
