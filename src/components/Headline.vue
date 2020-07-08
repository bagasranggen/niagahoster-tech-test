<template>
  <section class="headline">
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          PHP 7
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
}
</script>

<style lang="scss">
.headline {
  @extend %main-separator--bottom;

  padding-top: 50px;
  padding-bottom: 50px;
}
</style>
